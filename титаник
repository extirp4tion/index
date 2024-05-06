#!/usr/bin/env php
<?php
  echo "<br>";
  $age = $_GET['age'];
  $name =  $_GET['name'];
 print "выборка пользователей";
 if ($age != null) {
    print "&nbsp c возрастом &nbsp" . $age;
    $flag1=true;
}
else
{
    $flag1=false;
}
if ($name != null) {
    print " c именем " . $name;
    $flag2=true;
}
else
{
    $flag2=false;
}

$csvFile = 'titanic.csv';
if (($handle = fopen($csvFile, "r")) !== FALSE) 
{
    echo "<br>";
   while (($data = fgetcsv($handle, 1000, ",")) !== FALSE) 
   {
        if(stripos($data[2], "$name") !== FALSE && $data[4] == $age&&$flag1==true&&$flag2==true)
        {
            echo "<br>";
        foreach ($data as $value) {
            echo $value . "&nbsp&nbsp";
        }
    }
        else if($name !=null && strpos($data[2], $name) !== false  &&    $flag1==false)
{
    echo "<br>";
    foreach ($data as $value) {
        echo $value . "&nbsp&nbsp";
}
    }     
    else if($age !=null&& $data[4] == $age&&$flag2==false)
    {
        echo "<br>";
        foreach ($data as $value) {
            echo $value . "&nbsp&nbsp";
    }
    }
    else if ($name ==null &&$age ==null)
    {
        echo "<br>";
        foreach ($data as $value) {
            echo $value . "&nbsp&nbsp";
    }
    }
   }
    fclose($handle);
}
?>
