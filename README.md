# Sample_Project
## Stage-1(Frontend)
### Login Lorm(login.html)
1.User Input name=username
2.Passwod Input name=password

### Feedback Form(Index.html)
-Feedback Name Input name=f_name
-Feedback Email Inputname=f_email
-Feedback Rating Input name=f_rating
-Feedback Input name=feedback

### User data insert Form(User.html)
1.Company Name  Input name=c_name
2.Company Link Input name=c_link

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
-home
-login_views
-User_views
-admin_views
-feedback_approval
-feedback_delete
-logout_views

### App Urls ---->Function name with Nicknames
1.('',views.home,name='career'),
2.('login',views.login_views,name='login'),
3.('AdminPanel',views.admin_views,name='AdminPanel'),
4.('User',views.User_views,name='User'),
5.('approved/<int:pk>',views.feedback_approval,name='approved'),
6.('delete/<int:pk>',views.feedback_delete,name='delete'),
7.('logout',views.logout_views,name='logout')

### App Admin Register --->
-from Sample_app.models import Careers_hub
-from Sample_app.models import Career_feedback
#### Register models here.
-admin.site.register(Careers_hub)
-admin.site.register(Career_feedback)



