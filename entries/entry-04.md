
**In this blog**, I developed a better understanding of how to pick out HTML elements and apply dynamic interactivity to them with JS. The progress I have made compared to the last blog is visual, making it look a little more cohesive, and functional as well.

So far, I have added a delete button. The issue is that the delete button is not accurate, a problem I faced when first implementing my code. My code first collects the index of the current row the delete button is pressed in with `var i = x.rowIndex;`. Then, it locates the row from my tasks table with and the given index to delete it with `document.getElementById("myTasks").deleteRow(i);`. The delete button has the `onclick=”delRow(this)”`, `this` referring to the element getting this action done to it. When you click the trash icon, it only deletes the row on the very top. I tried to fix it by increasing `var i` by adding 1 or 2 if maybe the located `index` needed to surpass 0, but neither way worked, so I left it at that for now.

```svg:hover {
  fill: red;
}
```
Plus, I was able to create a CSS class to target the trash can `svg` icon (a small image) so when the mouse hovers over it, it turns red and indicates the row can be deleted.

I did not change much about the add new task button, but it looks different from the previous version. Something I figured would be useful to add were editable fields in the cells. To make it, each table row in the HTML file had to say `<td contenteditable='true'></td>`. The table data (`td`) is enclosed in a table row (`tr`), then a `table` tag.

An issue I did not anticipate was having the initial table header titles “Task, Notes, Due Date, Urgency, Done” be deleted by the trash icon too when pressed. So I created a separate table for the header without the `id=”myTasks”` the task list table has. The `delRow` class only works by accessing that id, so the initial header table is now safe from deletion.

Currently, the stage of the engineering design process I am in is _test and evaluate the prototype_. While creating the new features like editable fields and connecting buttons and table ids to functions, which added rows with a trash can to then delete them as I wished, I had to debug throughout the process and think about if my project was effective as a task list table so far, and it succeeds in this regard.

Some skills I am learning in this process are **logical reasoning and embracing failure**. In trying to create a delete button, there was resistance. While trying to create a new table that diverged from the original Eisenhower method tabs, I encountered difficulties in adding new tasks because they now required separate cells in a row. Looking back, the functions are fairly simple, but it took me time to think about how to connect an id or value to a button and table to later let me access it with JS. I tried a lot of things, and my code may even be repetitive and some parts may not be necessary to its function, but for now, it is my MVP, its fully functional in some ways and mildly annoying in others. Failure was plentiful in this stage, but giving up would have rendered the project to nothing, so I continued and brought it to the product I have now.

Similar to class, I found that writing functions and learning to break down the problem’s composition into simple ideas with the activities we did with Java also extended to how I used Javascript to get dynamic changes to occur within my table.

The sources I looked to throughout this project include lots of W3School. I found it helpful to look at simple examples where I could break down what each line of code did, and recreate it in my own project for a different use, as my table was more complicated in function. Or learning how to make my HTML elements connected to the JS for interactivity concerning buttons and all. Notable websites included: [Change Color of SVG on Hover | CSS-Tricks](https://css-tricks.com/change-color-of-svg-on-hover/), [The Many Ways to Link Up Shapes and Images with HTML and CSS](https://css-tricks.com/the-many-ways-to-link-up-shapes-and-images-with-html-and-css/), [HTML TableRow and rowIndex](https://www.w3schools.com/jsref/prop_tablerow_rowindex.asp), and [Event on-click JS](https://www.w3schools.com/jsref/event_onclick.asp).
