Message label plugin for roundcube

Attention! Latest version plugin use new roundcube class storage and don't work with version < 0.8.
For version < 0.8 use version plugin (1.0)
Require managesieve plugin for the filters.

Install
-------------------------------------------
1. git clone https://umount@github.com/umount/message_label.git message_label
2. move folder message_label in roundcube plugin folder
3. add 'message_label' to $rcmail_config['plugins'] in your RoundCube config


Introduction
----------------------------------------
This is plugin for roundcube to add labels like Google labels.

* manually and filter way add labels
* manually remove filter find labels
* multilabels support
* drag and drop to add label support
* remove label on one click on label in subject
* search all labels in all folder on one click (manual select folder search on filter search label) 
* display label list on left panel under folder list
* filters implemented with sieve require managesieve plugin to be installed

<h2>Instructions message_label</h2>

Create first label:<br/>
<img src="01_createFirstLabel.png">
<br/><br/>

Edit labels:<br/>
<img src="02_createLabel.png">
<br/><br/>

Create a filter that sets the label when the email comes in:<br/>
<img src="03_createFilter.png">
<br/>
Note: need to set the w flag for the user in Cyrus for this to work:
<pre>
cyradm --user cyrus-admin localhost
setacl user/max.mustermann@example.org max^mustermann@example.org w
</pre>
<br/><br/>
Manually assign labels:<br/>
<img src="04_markMessage.png">
<br/>
You can either use the Mark drop down menu, or drag the message to the label folder on the left side.<br/>
For removing a label from a message, you can just click the label in the message list.
