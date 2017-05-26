---
layout: post
title: Voicemail Notes v1
feature-img: "img/projects/voicemail-notes/feature-image.png"
thumbnail-path: "img/projects/voicemail-notes/400x300_icon.png"
short-description: Jot voicemail notes quickly.
date: "October 29th, 2016"
author: "Armando Cerrillo"
---

#### Bed, Bath & Beyond, anyone?
**explanation:**<br>
In a world slowly shying away from software bloat and increasingly favoring single serving apps I set out to create a lightweight & versatile note taking tool for jotting down, organizing and distributing guest messages throughout the company.

#### the land of lost post-it notes.
**problem:**<br>
Of the many tools utilized at work within the limitations of our thin-client computer terminals I have never been satisfied with having to take so many steps in jotting down, sorting and delegating voicemail messages. With a company of _over 100 staff & salon professionals_ it is at times daunting to know exactly which messages need to go where, in which format (i.e. print, e-mail, text) and the level of urgency of each request. This tool would allow the Guest Service team a much needed leg up on streamlining correspondence and minimize the number of post-it notes floating about the company, many lost in transit.

### Free the post-it!
**solution:**<br>
In order to group the functionality between the standard notepad, e-mail client and current message delegation system (print or otherwise) I set out 
to create a tool which would take each note, analyze it accordingly and supply the user options for distribution in a more streamlined manner. The first version has been to create a print-only version and in later iterations I plan to include auto-scanning for keywords as well as self-populating options for export dependent on the message content. For example if the term "reschedule" or "opinion" is found in realtime within the message body, a trigger would know the request to be for one of our salon professionals and given an option to print a css formatted note. If another message contains the word "manager" & "call-back" both a print option and e-mail option would be present along with the correct e-mail for the salon location manager.

### Utilization in practice
**results:**<br>
Utilizng Javascript & jQuery along with HTML & CSS for visual formatting and functionality I was able to create the first iteration of a printable version. Code is extremely light weight at this point and haven't had any issues with adding/deleting messages.

function **removeMessage()**:
```
$(event.target).parents('.message-body').remove();
    if (totalActiveMessages > 1 ) {
        totalActiveMessages -= 1;
    } else {
        setNewBlankMessage();
        totalActiveMessages = 1;
    }
    console.log(totalActiveMessages);
```

### Current Code & Future Modifications
**conclusion:**<br>
It has worked quite well for me the first few times and I have already imagined a few extra capabilities one could add such as user verification or the ability to include an 'undo-delete' method utilizing window.localStorage for the current session. I do plan on adding a search filter to the message which locates any phone numbers present in the message box and hoping to add e-mail buttons which would allow for message forwarding.

check-out the [full app here]

[full app here]: https://cerrillomedia.github.io/voicemail-notes-v1/