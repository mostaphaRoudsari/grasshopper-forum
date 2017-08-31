# grasshopper-forum

A snapshot of [Ladybug Tools forum on Grasshopper3d website](http://www.grasshopper3d.com/group/ladybug/forum) on 30 August 2017 in `json` format.

These files are created as for transferring from the [old forum](http://www.grasshopper3d.com/group/ladybug/forum) to the [new forum](http://discourse.ladybug.tools).


# Content

### discussions.txt
List of all the links to discussions on the Grasshopper forum which can be [accessed on-line at this link](http://www.grasshopper3d.com/group/ladybug/forum).

### members.txt
List of members data on the Grasshopper forum which can be [accessed on-line at this link](http://www.grasshopper3d.com/group/ladybug/user/list).

### ./data
A collection of json files. Each json file corresponds to a unique discussion or reply on the forum.
Discussions are named as `topic_[id].json` and replies are named as `reply_[id].json`.
Each reply has a `parent_id` tag that can be used to find the parent object.

Here is the strcuture of each object.

```javascript
  discussion = {
      'id': string,
      'topic': string,
      'created_by': string,
      'created_by_name': string,
      'created_at': datetime,
      'body': string,  // content of the reply as markdown
      'attachments': []  // list of attachments if any
  }


  reply = {
      'id': string,
      'created_by': string,
      'created_by_name': string,
      'created_at': datetime,
      'body': string, // content of the reply as markdown
      'attachments': [],  // list of attachments if any
      'parent_id': string
  }

  attachment = {
      'link': string,  // attachment link
      'name': datetime // attachment name
  }

```
