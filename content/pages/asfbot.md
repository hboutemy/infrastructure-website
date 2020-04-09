Title: ASF IRC services and archives

<p id="intro"> </p>

<a href="https://wilderness.apache.org/manual.html" target="_blank">ASFBot</a> on the <a href="https://freenode.net/" target="_blank">Freenode network</a> offers many services for Apache projects on Internet Relay Chat (IRC). IRC is an application layer protocol that facilitates text communication. The chat process works on a client/server networking model.

To enable these services, contact Infra, either with a <a href="https://issues.apache.org/jira/browse/INFRA" target="_blank">Jira ticket</a> or through `#asfinfra` on the official <a href="https://the-asf.slack.com/" target="_blank">Apache Slack instance</a>.

<h2 id="commits">Subversion, Git and Jira reporting</h2>

ASFBot can report on new commits to your Subversion or Git repository and or report when someone creates, updates, or closes a Jira ticket. You can tailor the ASFBot reports to your individual needs, with multiline logs, compacted paragraphs, coloring, different report styles, etc.

You can subscribe to any repository you like, and get reports on any specific changes you prefer, as long as these changes are publicly available. Subscriptions are <em>tag-based</em>, meaning that any one tag will apply to both Subversion and git commits.</p>

<h2 id="jiras">Reporting on Jira changes</h2>

If your channel is set up for Jira reporting, ASFBot keeps track of the latest changes to a Jira ticket. To view, for instance, the most recent comment pertaining to `INFRA-1234`, type: 

`ASFBot: comment INFRA-1234` 


<h2 id="issues">Fetching issue information</h2>

ASFBot can help you find the correct information or link related to specific Jira or Bugzilla issues. To use this feature for <code>issue #52230</code>, type:

`COUCHDB-1234`

ASFBot returns a link to that Jira ticket or Bugzilla issue and, if available, a short issue summary.

<h2 id="secretary">Secretary feature</h2>

ASFBot provides a simple secretary feature. To leave a message for an absent person, write: 

`ASFBot: tell [recipient] [message]`

ASFBot passees that message to the intended recipient the next time that person logs onto the channel.

<h2 id="meetings">Record keeping for meetings</h2>

ASFBot can keep a record of meetings you hold on IRC and publish these in HTML format with an agenda, actions to be taken and a list of participants. Record keeping is available in channels where logging is enabled. To enable logging, contact Infra.

Record keeping works as follows:

  - To initiate a meeting, type `ASFBot: meeting start`.
  - To set an agenda,type `#topic [agenda goes here]` or use the `/topic</` command to change the channel's topic. ASFBot will keep the original topic of the channel in memory, and change it back once the meeting is over.
  - To add information to the meeting summary, type `#info [something here]`.
  - Anything contributed with `[off]` at the beginning will be considered off-the-record and will not become part of the meeting log.
  - To add an action to be taken before the next meeting, type `#action [action]`.
  - To end a meeting and save a summary of it, type `ASFBot: meeting end`. This will end the record keeping and produce an HTML document containing the summary of the meeting and a log of everything participants wrote.
  - To send an IRC meeting summary as an email to a recipient, type `ASFBot: meeting send your@domain.tld`. You will need to have been granted karma by Infra to perform this task.

 ASFBot understands most <a href="https://meetbot.debian.net/Manual.html" target="_blank">meetbot</a> commands, so 
`#meetingstart` and `#meetingend` will also start and end a recording of a meeting.

For an example of what a meeting summary may look like, check out this record of a <a href="https://comments.apache.org/meetings/couchdb-meeting-16_01_2013-2439.html" target="_blank">CouchDB meeting</a>.

<h2 id="comments">Integration with comments.apache.org</h2>

ASFBot can relay comments provided via `comments.apache.org` to your IRC channel. If you have set up a karma list with Infra, you can also reply to comments via IRC.

<h2 id="sourcecode">Technical Information About ASFBot</h2>

  - The <a href="https://wilderness.apache.org/manual.html" target="_blank">ASFBot manual</a>
  = The ASFBot <a href="https://svn.apache.org/repos/infra/infrastructure/trunk/projects/asfbot/" target="_blank">source code</a>