Actually there's a very easy (built-in) method...

Go to admin/structure/views, find the view named Taxonomy term, and enable it
Go to admin/structure/views/view/taxonomy_term/edit
Click Advanced (on the right)
Click Content: Has taxonomy term ID (with depth)
Select a Depth of 1 or more
Save all your changes
Now, assuming the term id of Brand 1 is 1, 
when you visit www.yoursite.com/taxonomy/term/1, you should see all the child nodes listed. 
You can also create path aliases to make paths like taxonomy/term/1 more "pretty".
