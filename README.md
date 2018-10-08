# CRUD-Unit-Testing-

In General to perform crud operation most common,we can able to do in many ways.

Here I used spring boot and rest api,Mockito framework for writing unit test cases,As per MVC layer Model-View-Controller which I have Controller and Service,DAO.

Mainly I need to focus on the DAO layer,it's main layer to perform actual persistence operations,here I have used CrudRepository Interface to perform CRUD Operations such as Create-READ-Update-Delete.

In unit test case mainly need to focus on creating mock object and stubbing,once it has done,that's it gotcha.

The target class(mostly,DAO class) method what it should return,need give in external manner,then need to do stubbing,target class methods will be called inside the when condition and it will return (thenReturn) external given excepted result.

         when(dao.findById(1)).thenReturn(context);

Then to do so far assert that it means need to check equals or not.


