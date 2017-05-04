# SchedulerApi

* [Employee Availibility](#Avail)  
    * [Update](#AvailPut)
    * [Get](#AvailGet)

<div id="Avail">
<div id="AvailPut">

**Update Availibility**
----
    Updates an employee's availibility

* **URL**

  /employee/availibility/{EmployeeId}

* **Method:**

  `PUT`
  
*  **URL Params**

   **Required:**
 
   `EmployeeId=[integer]`

* **Data Params**

  ```C#
  //Data Table should contain Sun-Sat as column headers and hours as row headers
    DataTable EmployeeAvailibility;
  ```

* **Success Response:**

  * **Code:** 200 SUCCESS<br />

 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/users/1",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  </div>
  
 <div id="AvailGet"> 
 
**Get Availibility**
----
    Gets an employee's availibility

* **URL**

  /employee/availibility/{EmployeeId}

* **Method:**

  `Get`
  
*  **URL Params**

   **Required:**
 
   `EmployeeId=[integer]`

* **Data Params**
    none

* **Success Response:**

  * **Code:** 200 SUCCESS<br />
  **Content:**
  ```C#
  //Data Table should contain Sun-Sat as column headers and hours as row headers
    DataTable EmployeeAvailibility;
  ```

 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/users/1",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  </div>
</div>

<div id="notification">
**Get Notifications**
----
    Gets an Notifications

* **URL**

  /employee/Notifications/

* **Method:**

  `Get`
  
*  **URL Params**

   None
 
  

* **Data Params**
    None

* **Success Response:**

  * **Code:** 200 SUCCESS<br />
  **Content:**
  ```C#
  //contains a list of notifications
  List<Notification>
  //A notification will look like
   class Notification{
   int id
   int empl_id
   int message
   int isActive
  }
  ```

 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/users/1",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  </div>
</div>



## Employee Availibility

```C#
    //Eployee availibility
    //default everything is on
    
    
    //Datatable will be of bools
    
    public DataTable Get(){
      return DataTable;
    }
    
    public ActionResult Put(int id,DataTable){
      PutEmployeeVailRow();
    }
    
    Private PutEmployeeAvailrow(id, day, timeslot, bool){
    }
```



## Employee time off request

```C#
  class ViewModel{
    List<EmployeeNotifications>;
  }
  
  class EmployeeNotifications{
    string text;
    string url;
    string
  }
  
  class EmployeePageViewModel{
      DateTime Date;
      bool isAllDDay;
      List<string> hours;
      int StartHourId;
      int EndHourId;
 }
 
  public putUpdateNotification(Notification){}
  

  public List<Notifications> getNotifications(){}
  
  class Notification{
   int id
   int empl_id
   int message
   int isActive
  }
 
 EmployeeTimeOffRequest{
    int employeeId;
    int start;
    int end;
    bool? isApproved
 }
 
 public ActionResult PutTimeOffRequest{}
 
 
 
 public Json GetTimeOffResquest(int empId){}
    
```

```
classs configVar{
   string locationCode
   int id
   string name
   string  value
}
```
configVar getresoursceList(location, resource_id)
setresoursceList(configVar)
set(setore,input,fielD)
put StoreHurs(storeId, datatable)
dt getStoreHours(storeId)
dt getSemployeeschedulue (empl_id)
string setEmployeeSchedule(empl_id, dt)
set/view configuration

