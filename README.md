# Invention-Labs---SDE-Assignment-
A simple hospital management system with 3 basic entities --> Doctor, patient and Appointment. The database design used is MongoDB. 

Techstack used --> 
Java Spring Boot for enterprise application developement. (MAVEN BUILD) 
DEPENEDENCIES --> 
1) Spring boot starter data JPA
2) Rest Template
3) Lombok 
4) Swagger UI for API demonstrations  

Reason for MongoDB (noSQL style database) --> 
The entities were independent of eachother. No one-to-one/many-to-one relationships between doctor and patient. 

Project level assumptions --> 
1) DoctorId, PatientId and AppointmentId are auto-generated. [import org.springframework.data.annotation.Id;]
2) As the Ids are auto-generated, search by Id is not possible. (better security as well!!)
3) APPOINTMENT -- 
    a) When creating an appointment, only patientId, severity and speciality is taken as input. 
    b) When updating an appointment, doctorId and slot booking come into picture. 
    
    THUS, IF APPOINTMENT IS NOT UPDATED --> SLOT IS NOT BOOKED (slot=0; doctorId=null; Java does this by default)
4) The search results returns the following --> 
    id, firstName, lastname and userType. [userType is either Patient or Doctor] 
    
    Althought, we can search for a doctor or patient by firstName, lastName, age, speciality, phoneNumber, speciality & availability.
    
OVERALL -->
There are a total of 13 apis. 

Post Number - 8082

######################## IMPORTANT #######################
Once the spring boot application is running, please use this link to view the apis and its demonstration on swagger -->
http://localhost:8082/swagger-ui.html#/


Thank you for this opportunity to learn and grow :D

It was really fun!!
