---
layout: page
title: "Contact"
lang: en
ref: contact
permalink: /contact/
---

<form action="https://api.web3forms.com/submit" method="POST">
  <input type="hidden" name="access_key" value="cad6682d-f87e-41af-9c08-1efadc6646cd">
  <input type="hidden" name="subject" value="New message from kbuivan.com">
  <input type="hidden" name="from_name" value="kbuivan.com">
  <input type="hidden" name="redirect" value="https://kbuivan.com/contact/thanks/">
  <input type="checkbox" name="botcheck" style="display: none;">

  <p><label for="name">Name</label><br>
  <input type="text" id="name" name="name" required style="width:100%; padding:8px;"></p>

  <p><label for="email">Email</label><br>
  <input type="email" id="email" name="email" required style="width:100%; padding:8px;"></p>

  <p><label for="message">Message</label><br>
  <textarea id="message" name="message" rows="8" required style="width:100%; padding:8px;"></textarea></p>

  <p><button type="submit" style="padding:8px 20px;">Send</button></p>
</form>

<p><small>Your message is sent through the Web3Forms service and is used only to reply to you.</small></p>
