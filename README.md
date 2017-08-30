# grasshopper-forum

A snapshot of [Ladybug Tools forum on Grasshopper3d website](http://www.grasshopper3d.com/group/ladybug/forum) on 30 August 2017 in `json` format.

These files are created as for transferring from the [old forum](http://www.grasshopper3d.com/group/ladybug/forum) to the [new forum](http://discourse.ladybug.tools).


# Content

### discussions.txt
List of all the links to disscussions on the Grasshopper forum which can be [accessed on-line at this link](http://www.grasshopper3d.com/group/ladybug/forum).

### members.txt
List of members data on the Grasshopper forum which can be [accessed on-line at this link](http://www.grasshopper3d.com/group/ladybug/user/list).

### ./discussions
A collection of json files. Each json file corresponds to a unique discussion on the forum. In each file there will be a single discussion object.

Here is the strcuture of each object.

```javascript
  discussion = {
      'id': string,
      'topic': string,
      'created_by': string,
      'created_by_name': string,
      'created_at': datetime,
      'body': string,  // content of the reply as markdown
      'attachments': [],  // list of attachments if any
      'replies': [] // list of replies if any
  }


  reply = {
      'id': string,
      'created_by': string,
      'created_by_name': string,
      'created_at': datetime,
      'body': string, // content of the reply as markdown
      'attachments': [],  // list of attachments if any
      'replies': [] // list of replies if any
  }
  
  attachment = {
      'link': string,  // attachment link
      'name': datetime // attachment name
  }
  
```
