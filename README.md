A collection of useful web steps for **cucumber+capybara**

**List of steps provided, how to use them, and what they do.**

Fill out forms
--------------

<pre>
When I fill in [field name] with [value]
Ex: When I fill in "username" with "johndoe"
</pre>

Test content
------------

<pre>
Then I should see the text [whatever text you want]
Ex: Then I should see the text "Successfully logged in!"

Then I should see all of the texts:
  | the first text  |
  | the third text  |
  | the fourth text |

Then I should not see the text [whatever text should NOT appear]
Then I should see the image [the value of the "src" attribute]
Then I should see the image "test.png"
Then I should see all of the images:
  | test.png  |
  | about.png |
  | hello.png |

Then I should see a link that points to [value of the "href" attribute]
Ex: Then I should see a link that points to "http://example.com"
  
Then I should see a [tag] with [attribute name] of [attribute value]
Ex: Then I should see a "div" with "id" of "content-container"
</pre>

Test links, buttons, dialog boxes
---------------------------------

<pre>
When I follow [link]
  The "link" is the text, id, or name of any link on the page. This is the standard step.
When I press [button name]
  The "button name" is the text, id, or name of any button on the page. This is the standard step.
When I accept the confirmation dialog box
  Especially useful when you're testing javascript, or other actions that generate dialog boxes for your users, this step will switch to the dialog box, and click the accept option.
</pre>

Test navigation
---------------

<pre>
Given I go to [path name]
Ex: Given I go to the login page
Then I should be on [path name]
Ex: Then I should be on the new user page
</pre>

Other
-----

<pre>
Given pending
  Marks an entire scenario as pending.
When I wait 3 seconds
  Pause the web driver for the specified number of seconds. For example, you want to test AJAX which fires after 500 milliseconds, have the web driver wait 1 second.
Then debug
  Inserts a "debugger" step. You must have `ruby-debug` or a similar gem installed for this step to actually pause.
</pre>