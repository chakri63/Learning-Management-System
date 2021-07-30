# Learning-Management-System
Create a cloud-based platform for teachers to upload and schedule - notes, flowcharts, diagrams, videos, presentations,
and others. Educators should be allowed to plan, organize, and display the curriculum for upcoming weeks for increased 
transparency.

Identify and execute apps that allow different users, such as—students, parents, and teachers—to post questions, 
reply to comments, and tag relevant subjects and users.


-Class
--subject 
---daily schedule 
---- notes, video, animation, ppt etc (study material)
------comments and replies (by anyone )

	
required apps: courses and users 

class models: 
- courses: class, subject, lesson, comments
- users: custom user model 

USERS: teachers, student, parents 


users model:  
- name (one to one with django user model)
- bio
- profile pic
- user_type 
** different user types will have different accessibility


class model: 
- name of class (10, 11 etc.) (id)
- description 

subject model: 					
- subject_id (id)
- subject name 			
- class (foreign key)	
- image 		
- description 

lesson model: 
- lesson_id (id)
- standard (foreign key)
- created by (user - foreign key)
- created at
- subject (foreign key)
- lesson_name 
- position (chapter no.)
- video
- ppt
- notes

Comment model:
- lesson name (foreign key)
- comm_name 
- author (user -foreign key)
- body 
- date_added (datetime)


reply model:
- comment_name (foreign key)
- reply_body 
- author (user -foreign key)
- date_added (datetime)
