# Sample_Project
## Stage-1(Frontend)
### Login Lorm(login.html)

###### User Input name=username
###### Passwod Input name=password

### Feedback Form(Index.html)

###### -Feedback Name Input name=f_name
###### -Feedback Email Inputname=f_email
###### -Feedback Rating Input name=f_rating
###### -Feedback Input name=feedback

### User data insert Form(User.html)

###### * Company Name  Input name=c_name
###### * Company Link Input name=c_link

## Stage-2 Database(Models)
## App Models
### Career_hub--->Class name

| Attributes    | Models Fields | Constraints    |
| ------------- |:-------------:|---------------:|
| company_name  | CharField     | max_length=30  |
| company_link  | TextFiels     | max_length=100 |

### Career_Feedback--->Class name

|Attributes     | Models Fields   | Constraints                     | 
| --------------|:---------------:|--------------------------------:|
| fullname      | CharField()     | max_length=30                   |       
| email         | emailField()    |                                 |
| rating        | IntegerField()  |                                 |
| feedback      | CharField()     | max_length=500                  |
| status        | CharField()     | default="pending",max_length=20 |


## Stage-3 Backend 
### App Views---->(Function names)
###### 1.home
###### 2.login_views
###### 3.User_views
###### 4.admin_views
###### 5.feedback_approval
###### 6.feedback_delete
###### 7.logout_views

### App Urls ---->Function name with Nicknames

|   Route             |   Views Name            |   Nicknames                     | 
| --------------------|:-----------------------:|--------------------------------:|
| ''                  | views.home              |  name='career'                  |       
| 'login'             | views.login_views       |  name='login'                   |
| 'AdminPanel'        | views.admin_views       |  name='AdminPanel'              |
| 'User'              | views.User_views        |  name='User'                    |
| 'approved/<int:pk>' | views.feedback_approval |  name='approved'                |
| 'delete/<int:pk>'   | views.feedback_delete   |  name='delete'                  |
| 'logout'            | views.logout_views      | name='logout'                   |


### App Admin Register --->
###### * from Sample_app.models import Careers_hub
###### * from Sample_app.models import Career_feedback
#### Register models here.
###### -admin.site.register(Careers_hub)
###### -admin.site.register(Career_feedback)



