# Data Analytics Week at the Loft
## Visualization with Amazon QuickSight

prerequisite: [Redshift Basics](https://github.com/wrbaldwin/da-week/blob/master/Labs/Redshift-Basics.md)

In this lab exercise, you will set up a QuickSight account, then visualize the data you entered in the “Using Redshift” Hands-on Lab. You will need a Mac or Windows computer with a Firefox or Chrome browser.

1.	Set up your QuickSight Account
*	From the AWS Console, choose the QuickSight service
*	Choose **Sign Up for Quicksight**
*	Select **Standard** edition, then choose **Continue**
*	In the QuickSight account name box, type myQuickSight
*	In the Notification email address box, type your email address
*	Select the AWS region assigned by your instructor
*	Be sure the boxes are checked for “Enable autodiscovery of data and users in your Amazon Redshift, Amazon RDS and AWS IAM services.” And “Amazon Athena”
*	Choose **Finish**
*	Once the account is created, view the welcome screens

2.	Create an analysis from your Redshift data
*	Choose **New Analysis**, then **New Data Set**
* Select Redshift Auto-discovered
*	In the New Redshift data source panel, enter:

```
Data source name = myRedshiftData
Instance ID = examplecluster
Database name = dev
Username = masteruser
Password = __the password you created for Redshft__
```

*	Choose **Create data source**
*	In the Choose your table panel, select none of the tables and choose **Edit/Preview Data**
* Click **Save**

3. Create another analysis from your Redshift data
*	Create a new dataset with sales by date
*	Delete any tables shown, then add the date and sales tables
*	Click on the join (two red circles), then configure an inner join that uses date.dateid and sales.dateid, then choose **Apply**
*	Name the dataset salesByDate, then choose **Save & Visualize**

4.	Visualize sales by date
*	In the Visual Types pane, choose a Vertical bar chart
*	Drag caldate from Fields list to the X axis
* Drag qtysold(sum) from Fields list to Value
*	Explore the visualization of your data
*	Choose **Share**, then **Publish Dashboard**
* Give your new dashboard a name and click **Publish dashboard**
* Close the Share with Users box

4.	Create more visualizations
*	Add new datasets and visualizations to your dashboard. Can you show top buyers by last name? Top events by sales?
[Hint: see the queries from the Using Redshift lab to identify the right tables and fields.]

