student={}
def add():
   name=input("Enter the name of student: ")
   grade =input("Enter the grade of student: ")
   student["name"]=grade
   print("Student details added successfully")
def delete():
   name=input("Enter the name of student to delete: ")
   if name in student:
      del student[name]
      print("Student details deleted successfully")
   else:
      print("Student not found")
def search():
   name=input("Enter the name of student to search: ")
   if name in student:
      print(f"Student Name: {name}, Grade: {student[name]}")
   else:
      print("Student not found")
def display():
   if student:
      print("*****STUDENT DETAILS*****")
      for name, grade in student.items():
         print(f"Student Name: {name}, Grade: {grade}")
   else:
      print("No student details available")
def exit():
   print("Exiting the program.")
   quit()


while True:
   print("*****STUDENT DETAILS*****")
   print("1. Add ") 
   print("2. delete")
   print("3. search")
   print("4. display")
   print("5. exit")
   choice=int(input("Enter your choice:"))
   if choice==1:
      add()
   elif choice ==2:
      delete()
   elif choice ==3:
      search()
   elif choice ==4:
      display()
   elif choice ==5:
      exit() 
