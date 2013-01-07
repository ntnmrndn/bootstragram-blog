---
layout: default
title: Creating Post-it like Scrum Cards from Jira export with jQuery and CSS
---

# Making Scrum Cards from Jira with jQuery and CSS

<p class="lead">
  Sometimes you run out of Post-Its. Shit happens. Let's keep the task board busy anyway...
</p>

It happened to me in real-life. We just agreed on our Sprint backlog and are willing to display it proudly on our walls but... there's no Post-Its left. What are your options then?

- you can just run to the local store... Sure but come on. This chair is comfortable.
- you can find a plugin for your bug-tracker (let's just assume you're using Jira too, ok?) like [this one](https://marketplace.atlassian.com/plugins/com.spartez.scrumprint.scrumplugin) but what if you're using the "OnDemand" version?

Well, then Jira's export functions and some basic jQuery and CSS can help.

## Jira export

In the "Issues" tab, select your filter, and then "Views" and "Excel (Current Fields)". Wait what?! We're going to use Excel?! Hell no. Keep calm and carry on. This kind of export is just a HTML file. Weird but kind of convenient. Rename this file with a <code>.html</code> extension, open it in a browser and a text editor: the magic is about to open.

## The Magic of jQuery and CSS

Head to [this GitHub repo](https://github.com/dirtyhenry/jira-to-agile-cards), copy the two files included in the same directory where you have your .html file and add the following 2 lines at the end of your Jira export:

    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js"></script>
    <script src="jira.js"></script>
    
And refresh your HTML page. Tada!

## Troubleshooting

If the "tada" moment is more of a "nothing happened" moment, check out your JavaScript console: it's most likely a jQuery download failure. In which case, download jQuery and change the above script to include a local version of jQuery.

If it's still not working, try to get some context and yell at me [here](https://github.com/dirtyhenry/jira-to-agile-cards/issues).