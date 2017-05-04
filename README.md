# SchedulerApi


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
   id
   empl_id
   message
   isActive
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
