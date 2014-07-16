
![Pquery Logo](http://res.cloudinary.com/gatec21/image/upload/c_scale,w_271/v1403196836/pQuery_l0bq3z.png) 
    
    powerShell Web automation simplified! Inspired by jQuery's ease of use.


*pQuery is a work in progress. Forks/Pulls Welcome.* 


This module is meant to create a variable that we can use jQuery-like syntax to do jQuery-like
manipulations on a website.

## Install

1. Download repository
2. Unzip. Unlock .dll files in pQuery directory. (Right click file->Properties->Unblock->OK).
3. Move pQuery folder to %UserProfile%\Documents\WindowsPowerShell\Modules
3. Open up PowerShell and import the module
	* Import-Module pQuery

## CORE

#### Find members attached to $pQuery variable 
    $pQuery | GM

#### Initialize pQuery
*This should be the first function that you run.*

	$pQuery.Init()

#### Set headers for basic authentication
*Only needed if site is behind basic authentication.*

    $pQuery.setCredentials("username:password")
	
#### Navigate to the site specified


    $pQuery.Navigate("http://github.com/misterGF")



## USAGE
*Types can be button, div, form, input or a.*


#### Viewing HTML of current page!
    
    $pQuery.getHTML()




#### Selecting!
    
    $pQuery.Select("button") #By Type
    
    $pQuery.Select("#button") #By ID
    
    $pQuery.Select(".button") #By Class





#### Getting Text!
    $pQuery.getText("button") #By Type
    
    $pQuery.getText("#button") #By ID
    
    $pQuery.getText(".button") #By Class



#### Setting Text!
*Set the text value based on your selector. Optionally return boolean value*

    $pQuery.setText("button","My Modified Text") #By Type
    
    $pQuery.setText("#button","My Modified Text") #By ID
    
    $pQuery.setText(".button","My Modified Text", $true) #By Class and optionally return $true or $false. Useful for unit testing.



#### Clicking!
*Currently Supporting buttons and links.*

    $pQuery.click("#greenBtn") #By ID
    
    $pQuery.click(".buttons", $true) #By Class and optionally return $true or $false. Useful for unit testing.

#### Submitting!
*Submit a form.*

    $pQuery.submit("#formBtn") #By ID
    
    $pQuery.submit(".formBtn", $true) #By Class and optionally return $true or $false. Useful for unit testing.
