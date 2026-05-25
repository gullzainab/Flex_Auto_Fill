# Flex_Auto_Fill
Built a small automation tool for FAST FLEX Faculty Feedback 🚀
One thing that always annoyed me every semester was manually filling the faculty feedback forms repeatedly for every course.

So after multiple trials and testing, I created a simple browser bookmark automation that can:
✔ Auto-fill the feedback form
✔ Auto-submit it
✔ Save a lot of repetitive effort

Currently tested on limited users and working successfully.

How it works:
For Google/Chrome Browser(However it can work for any browser but do proper pasting of URL)
Click
 "Open bookmark manager"
In Bookmark Manager:
Click the three dots (⋮) at the top right
Click "Add new bookmark"
In Name type: 
FLEX Auto Fill(or Any name of your choice)
In URL paste this code:

javascript:(function(){var radios=document.querySelectorAll('input[type=radio]');var names={};for(var r of radios){if(!names[r.name]){names[r.name]=r;r.click();}}var filled=Object.keys(names).length;var btns=document.querySelectorAll('input,button');for(var b of btns){var t=b.innerText||b.value||'';if(t.toLowerCase().includes('submit')){b.click();break;}}alert('Filled '+filled+' questions and submitted!');})();

Click Save
Next,
Go to FLEX and log in
Go to Course Feedback page
Click Give Feedback for Course 1
When the feedback form opens, click Flex_Auto_Fill bookmark
It will fill everything and submit automatically!
Repeat this process for all other courses.
This was a small but interesting experiment in browser-side automation using JavaScript.
Thankyou
