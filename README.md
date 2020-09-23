<div align="center">

## Date Picker


</div>

### Description

This javascript will get the number of days in a month based upon the year selected.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[masterp](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/masterp.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/masterp-date-picker__2-2607/archive/master.zip)





### Source Code

```
<SCRIPT LANGUAGE="JavaScript">
function populate(objForm,selectIndex)
{
   timeA = new Date(objForm.year.options[objForm.year.selectedIndex].text,   objForm.month.options[objForm.month.selectedIndex].value,1);
   timeDifference = timeA - 86400000;
   timeB = new Date(timeDifference);
   var daysInMonth = timeB.getDate();
   for (var i = 0; i < objForm.day.length; i++)
   {
     objForm.day.options[0] = null;
   }
   for (var i = 0; i < daysInMonth; i++)
   {
     objForm.day.options[i] = new Option(i+1);
   }
   document.f1.day.options[0].selected = true;
}
function getYears()
{
// You can customize what years can be used
  var years = new Array(1997,1998,1999,2000,2001,2005)
  for (var i = 0; i < document.f1.year.length; i++)
  {
     document.f1.year.options[0] = null;
  }
  timeC = new Date();
  currYear = timeC.getFullYear();
  for (var i = 0; i < years.length; i++)
  {
     document.f1.year.options[i] = new Option(years[i]);
  }
  document.f1.year.options[2].selected=true;
}
window.onLoad = getYears;
</script>
</HEAD>
<BODY>
<center>
<form name=f1>
<table border=0>
<tr>
<td align=center>
<select name=year onChange="populate(this.form,this.form.month.selectedIndex);">
<option selected value=99>1999</option>
<option value=00>2000</option>
<option value=01>2001</option>
<option value=02>2002</option>
<option value=03>2003</option>
<option value=04>2004</option>
<option value=05>2005</option>
</select>
<select name=month onChange="populate(this.form,this.selectedIndex);">
<option value=01>January</option>
<option value=02>February</option>
<option value=03>March</option>
<option value=04>April</option>
<option value=05>May</option>
<option value=06>June</option>
<option value=07>July</option>
<option value=08>August</option>
<option value=09>September</option>
<option value=10>October</option>
<option value=11>November</option>
<option value=12>December</option>
</select>
<select name=day>
<option> </option>
<option> </option>
<option> </option>
<option> </option>
<option> </option>
<option> </option>
<option> </option>
</select>
</td>
</tr>
</table>
</form>
</center>
```

