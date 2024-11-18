# FOREIGN KEY!!!
tables: employees, reference, schedule, users

SELECT e.id, e.name, e.department, e.station, e.rest_day, e.remarks, e.is_student, e.suspended, e.user_id
FROM employees e
JOIN kitchen_department kd ON e.department = kd.departmentID
JOIN kitchen_station ks ON e.station = ks.stationID;
                                                 
sql table: employees
rows: id | name | department | station | rest_day | remarks | is_student | suspended | user_id
		  (Dapat INT) (Dapat INT)      
		  (  kd.departmentID & ks.stationID  )

TODO: 
	Create a table for department & station
	- KitchenDepartment
	- KitchenStation
	- ServiceDepartment
	- ServiceStation

sql table: kitchen_department 	sql table: kitchen_station
rows: id | departmentID		rows: id | stationID