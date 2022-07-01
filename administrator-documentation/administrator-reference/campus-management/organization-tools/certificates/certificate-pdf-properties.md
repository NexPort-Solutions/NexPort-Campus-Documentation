---
description: These are the available fields in the Nexport Certificates
---

# Certificate PDF Properties

## Available Certificate Fields

### **Basic Fields**

01    first.name\
02    middle.name\
03    last.name\
04    name : "First Last"\
05    formalname : "Last, First Middle"\
06    nickname\
07    user.title\
08    user.email\
09    course.title\
10    section.description\
11    section.title\
12    section.number

## Available Date Fields

### **Date the user enrolled in the course.**

1    enrollment.fulldate\
2    enrollment.simpledate\
3    enrollment.shortdate\
4    enrollment.shortdatetime

### **Date the user last saved data for the course (e.g. the date they completed the course).**

1    last.activity.fulldate\
2    last.activity.simpledate\
3    last.activity.shortdate\
4    last.activity.shortdatetime

### **Date that the certificate was created**

1    current.fulldate\
2    current.simpledate\
3    current.shortdate\
4    current.shortdatetime

### **Date that the subscription was created**

1    subscription.created.fulldate\
2    subscription.created.simpledate\
3    subscription.created.shortdate\
4    subscription.created.shortdatetime

### **Date that the subscription will expire**

1    subscription.expires.fulldate\
2    subscription.expires.simpledate\
3    subscription.expires.shortdate\
4    subscription.expires.shortdatetime

### Date Formats

* `.fulldate`: Tuesday, 22 August 2006, 6:30 AM
* `.simpledate`: Tuesday, 22 August 2006
* `.shortdate`: 8/22/2006
* `.shortdatetime`: 8/22/2006, 6:30 AM

## Available Student Contact Information

* student.FirstName
* student.LastName
* student.MiddleName
* student.Title
* student.Nickname
* student.PrimaryEmail
* student.AddressLine1
* student.AddressLine2
* student.FullAddress
* student.City
* student.State
* student.Country
* student.PostalCode
* student.Phone
* student.Mobile
* student.Fax
* student.Caption

## Custom Profile Field Format

* **Field Name:** student.ExtendedProfile.PROFILEFIELDKEY.Name
* **Field Description:** student.ExtendedProfile.PROFILEFIELDKEY.Description
* **Field Value:** student.ExtendedProfile.PROFILEFIELDKEY.Value

## Custom Enrollment Field Format

* **Field Name:** enrollment.Fields.ENROLLMENTFIELDKEY.Name
* **Field Description:** enrollment.Fields.ENROLLMENTFIELDKEY.Description
* **Field Value:** enrollment.Fields.ENROLLMENTFIELDKEY.Value

#### &#x20;© NexPort Solutions 2022. All Rights Reserved. 
