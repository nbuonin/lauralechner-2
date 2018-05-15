---
title: Contact
permalink: "/contact/"
layout: contact
---

<div class="container narrow">
    <p id="contact-message">Please, get in touch if you'd like to work together.</p>
    <form id="contact-form" action="//formspree.io/laura@lauralechner.com"
                            method="POST">
        <label for="name">Name</label>
        <input type="text" name="name" id="name" required>
        <label for="message">Message</label>
        <textarea type="text" name="message" id="message" required></textarea>
        <label for="email">E-Mail Address</label>
        <input type="email" name="_replyto" id="email" required>
        <input type="hidden" name="_next" value="/#contact-form" />
        <input type="text" name="_gotcha" style="display:none" />
        <input type="submit" value="Send">
    </form>
    <div id="success">
        <p>Thanks for your note.  I'll be in touch soon.</p>
    </div>
    <div id="error">
        <p>Huh, looks like there was a problem with the form.  Please try again.</p>
    </div>
</div>
