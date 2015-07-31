# swing-components
Automatically exported from code.google.com/p/swing-components

Swing Components is library that provides common user interface controls that aren't in the standard Swing toolkit.

Controls currently in the library

    1. [JCalendarWidget](http://naveedmurtuza.blogspot.com/2011/04/jcalendarwidget.html)
    2. [JDatePicker](http://naveedmurtuza.blogspot.com/2011/04/jcalendarwidget.html)
    3. [JButtonMenuItem](http://naveedmurtuza.blogspot.com/2011/01/jbuttonmenuitem.html)
    4. [JSplitButton](http://naveedmurtuza.blogspot.com/2010/11/jsplitbutton.html)
    5. JIPTextField
    6. JCheckboxList
    7. Column Manager 

JCalendarWidget,JDatePicker,JButtonMenuItem &amp; JSplitButton has already been posted on my [blog](http://naveedmurtuza.blogspot.com/) and on google projects. For more details on them please navigate to the links provided in the list.

##5. JIPTextField:

JIPTextField is IP Address Control supporting both IPV4 &amp; IPV6. The functionality of JIPTextField is similar to the IP Address control found in Windows. For an example, if the value entered is greater than 255 then it defaults to 255. Also, you can use Tab to navigate from one octet to another within the JIPTextField.

###Screenshots: 

![JIpTextField1](https://raw.github.com/akuhtz/swing-components/master/wiki/images/JIpTextField1.png)

![JIpTextField2](https://raw.github.com/akuhtz/swing-components/master/wiki/images/JIpTextField2.png)

###Usage:
```java
JIpTextField ipField = new JIpTextField();
//add it to GUI

//set ip address
ipField.setText("192.168.1.1");
//or 
ipField.setAddress(Inet4Address.getByName("192.168.1.1"));

//get the ip address
int[] octects = ipField.getOctects();
//returns -&gt; octects[0] = 192;octects[1] = 168;octects[2] = 1;octects[3] = 1;

//to get the ip address as string
String ip = ipField.getText();
String ip1 = ipField.getIpAddressString();

//to get the ip as an instance of InetAddress
InetAddress addr  = ipField.getIpAddress();
```

##6.JCheckboxList

A list where each item has a checkbox in it. With each item in a list being an instance of JCheckbox, the list selection is independent to checkbox selection. As with all the other visible beans in this library, this can be added to the IDE's palette.

Use getCheckedIndices() and getCheckedItems() to get the items that are checked in the CheckboxList. For a screenshot of, see screenshot 2 of Column Manager.

##7.Column Manager

Table Column Chooser attaches a popup menu on the JTable header, when the user right-clicks on the header a popup menu appears allowing the user to show or hide columns from the view, resize the columns and arrange the columns.

###Screenshots: 

![TableColumnManager1](https://raw.github.com/akuhtz/swing-components/master/wiki/images/TableColumnManager1.png)

###Usage:
```java
//thats all there is to it!
TableColumnChooser tableColumnChooser = new TableColumnChooser(jTable.getTableHeader());
tableColumnChooser.install();
```
The popupmenu that appears allows users to show and hide columns in the table.A column can be shown or hidden through the popup menu, as well as programmatically. To resize all columns to fit within the current viewport, select Size All Columns to Fit from the popup. Programmatically, you can do this using the packAll() and packColumn(int vColIndex, int margin) methods.
```java
// true to show the column, false to hide it.
tableColumnChooser.toggleColumnVisibility("Title1",true); 
```

