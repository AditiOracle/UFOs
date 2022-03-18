# UFOs
Module 11 Javascript
**Module 11**

**Challenge – UFO Finder**

**Overview of Project:**

We have designed the webpage to search the UFO information based on the different values entered in the input boxes.

- First we created the index.html page which has reference to our data.js (which hosts the data), app.js (hosts our JavaScript code) and D3 library.
- In this index.html file we created a table with just header cells in it.
- Then in app.js file we brought the data from data.js file and then rendered in tabular form on HTML file - by selecting the `tbody` tag and appending the `\&lt;tr\&gt;` tag and then adding the `\&lt;td\&gt;` tag to `\&lt;tr\&gt;` tag and then add the text value in `\&lt;td\&gt;` tag.

We created the event handler on change event for all \&lt;input\&gt; tags.

Then we created an object: &quot;filters&quot; where we will store the filtered values from the input boxes that we want to match on the table data.

Next, we created `updateFilters()` function to retrieve the HTML tag, its value and its ID.

And saved the tag id and it&#39;s value in filter object as key value pair.

In the same function we called the `filterTable()` function which is created to match the Object: `filters` key and value pair to the `tableData` key and value pairs by loop through each element in filters object and used the filter method to go through `tableData`.

**RESULT:**

The user has to type the value in the input box and the based on the input value the results will be shown in the table. User has to press the Tab key or Enter key from keyboard to search the data. Search is case sensitive.

For example: if you enter the city – `benton` then the table will show us the record belongs to Benton city and there is only one record that belongs to `benton`.

![Search on City]()

Enter a city: bonita

Enter a Country: us

It will give you results based on these two filters

![Search on City and Country]()

![Search on all field values]()

**Summary:**

There are lots of flaw in this new design:

**Header Cell Formatting** : We can have separate color and formatting for header cells, to distinguish them from the row data.

**No Validation on Text Entered** : There are no validation checks on the input boxes: If we enter the wrong format of the date then it should show us warning message: Input the date in right format – MM/DD/YYYY

**Drop Downs \&lt;select\&gt; in place of Text boxes** : There should be drop downs (select option tag) for City, State, and Country and Shape fields. For date also there should be some kind of Calendar for date field.

**Data is not formatted properly** : City, State and Country are in lowercase. Duration column has _no consistent values_. Some places it has min, mins, minutes, downtown, 10:00.

Shapes field also has some weird entries – disk, light, formation, chevron, other, teardrop

**ETL should be on done** : We should perform the ETL on our data before rendering it on the website.

**Error/Warning Message** : When there is no data found for the values entered, it should show us some message – No Data Found!

**Drop Down directly on top navigation pane** : There can be filters directly on navigation bar. It will easy search for the client then there is no need of separate form that we have designed.

**Search should not be case sensitive.**