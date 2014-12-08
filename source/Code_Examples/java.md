---
layout: page
weight: 0
title: Java
navigation:
  show: true
---
{% github sendgrid/sendgrid-java#usage Java %} We recommend using SendGrid Java, our client library, <a href="https://github.com/sendgrid/sendgrid-java">available on Github</a>, with full documentation. {% endgithub %}

{% anchor h2 %} Using SendGrid's Java Library {% endanchor %}
{% codeblock lang:java %}
// using SendGrid's Java Library - https://github.com/sendgrid/sendgrid-java
import com.sendgrid.*;
 
public class SendGridExample {
  public static void main(String[] args) {
    SendGrid sendgrid = new SendGrid(api_user, api_key);
 
    SendGrid.Email email = new SendGrid.Email();
 
    email.addTo("test@sendgrid.com");
    email.setFrom("you@youremail.com");
    email.setSubject("Sending with SendGrid is Fun");
    email.setHtml("and easy to do anywhere, even with Java");
 
    SendGrid.Response response = sendgrid.send(email);
  }
}
{% endcodeblock %}
