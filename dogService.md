# dog-
All information for dog




import java.util.Scanner;
import java.io.File;
import java.util.Date;

public class Dog extends newDogFile{
    
    public int dogCubby;
    public String dogFirstname;
    public String dogLastname;
    public String dogBreed; 
    public String parentFirstName;
    public String parentLastName;
    public String parentAddress; 
    public String parentPhoneNumber; 
    
    
    
    
    
    /**
     * Constructor for objects of class Dog
     */
    
    public void Dog(int cubby, String firstName, String lastName, String breed, String ownerFirstName, String ownerLastName, String ownerAddress, String ownerPhoneNumber)
    {
        dogCubby = cubby; 
        dogFirstname = firstName; 
        dogLastname = lastName; 
        dogBreed = breed; 
        parentFirstName = ownerFirstName;
        parentLastName = ownerLastName; 
        parentAddress = ownerAddress; 
        parentPhoneNumber = ownerPhoneNumber; 
        
        
    }

    public void setCubby(int cubby){
        dogCubby = cubby; 
    
    }
    public int getCubby(){
        return dogCubby; 
    }
    
    public void setFirstname(String firstName){
        dogFirstname = firstName;
    }
    
    public String getFirstname(){
        return dogFirstname; 
    }
    
    public void setLastname(String lastName){
        dogLastname = lastName; 
    }
    
    public String getLastname(){
        return dogLastname; 
    }
    
    public void setdogBreed(String breed){
        dogBreed = breed; 
    }
    
    public String getBreed(){
        return dogBreed; 
    }
    
    public void setParentFirstName(String ownerFirstName){
        parentFirstName = ownerFirstName;
    }
    
    public String getParentFirstName(){
        return parentFirstName; 
    }
    
    public void setParentLastName(String ownerLastName){
        parentLastName = ownerLastName; 
    }
    
    public String getParentLastName (){
        return parentLastName; 
    }
    
    public void setParentAddress(String ownerAddress){
        parentAddress = ownerAddress; 
    }
    
    public String getParentAddress(){
        return parentAddress; 
    }
    
    public void setParentPhoneNumber(String ownerPhoneNumber){
        parentPhoneNumber = ownerPhoneNumber; 
    }
    
    public String getParentPhoneNumber(){
        return parentPhoneNumber; 
    }
    
    public String dogBasicInfo(){
        System.out.println("Cubby number: " + dogCubby); 
        System.out.println("Dog first name: " + dogFirstname); 
        System.out.println("Dog last name: " + dogLastname);
        System.out.println("Dog's breed: " + dogBreed); 
        return "";
        
    }

    public String toString(){
        return "This dog's name is " + dogFirstname + " " + dogLastname + " and " + dogFirstname + " is a " + dogBreed + ". " + dogFirstname + "'s cubby number is " + dogCubby; 
    }

    public static void dogService(tenure info){
   
        Scanner sc = new Scanner(System.in);
        System.out.println("Is this dog new?(yes/no): ");
        String newDog = sc.nextLine();
        if (newDog.equals("yes")){
            //dog parent info
            tenure dog = new tenure();
            System.out.println("Dog's Parent's First Name; ");
            String parentFirstName = sc.nextLine();
            dog.setParentFirstName(parentFirstName);
            System.out.println("Dog's Parent's Last Name: ");
            String parentLastName = sc.nextLine();
            dog.setParentLastName(parentLastName);
     
            //dog basic info
            System.out.println("Dog's First Name: ");
            String firstName = sc.nextLine();
            dog.setFirstname(firstName);
            System.out.println("Dog's Last Name: ");
            String lastName = sc.nextLine();
            dog.setLastname(lastName); 
            System.out.println("Dog's breed: ");
            String breed = sc.nextLine();
            dog.setdogBreed(breed);
         
            //dog info if staying 
            System.out.print("Is " + firstName + " " + lastName + " here for a service?(yes/no):  "); 
            String hereForService = sc.nextLine();
            System.out.println("");
            if (hereForService.equals("yes")){
             System.out.print(firstName + "'s cubby number: ");
             int cubby = sc.nextInt();
             dog.setCubby(cubby);
             sc.nextLine();
             
             System.out.print("Arrival date: ");
             String arrival = sc.nextLine();
             dog.setArrival(arrival);
             System.out.println("Departure date: "); 
             String departure  = sc.nextLine();
             dog.setDeparture(departure); 
             System.out.println("Time out: "); 
             String timeOut = sc.nextLine(); 
             dog.setTimeout(timeOut);
             System.out.println("Is " + firstName + " " + lastName + " here for Boarding, Grooming, Daycare: "); 
             String service = sc.nextLine(); 
             if (service.equals("boarding")){
                 dog.setBoardingService(service);
                 //ENTER THE PRICE FOR THE BOARDING (DEPARTURE DATE-ARRIVAL DATE
                 
                 System.out.println("Is " + firstName + " being groomed?(yes/no): "); 
                 String groom = sc.nextLine(); 
                 if (groom.equals("yes")){
                     System.out.print("What groom Service(s): ");
                     String groomService = sc.nextLine(); 
                     dog.setGroomService(groomService); 
                     System.out.print("Groom price: ");
                     float groomPrice = sc.nextFloat();
                     dog.setGroomCost(groomPrice);
                     sc.nextLine();
                     System.out.println("");
                     System.out.println(dog.dogBasicInfo());
                     System.out.println(dog.dogInfo());
                    }
                }
             else if (service.equals("daycare")){
                 dog.setDaycareService(service);
                 System.out.print("Daycare cost: ");
                 float daycareCost = sc.nextFloat(); 
                 dog.setCostDaycare(daycareCost); 
                 sc.nextLine();
                 System.out.println(""); 
                 System.out.println(dog.dogBasicInfo());
                 System.out.println(dog.dogInfo());
                 
                }
             
             else if (service.equals("grooming")){
                   dog.setGroomService(service);
                   System.out.print("What groom Service(s): ");
                   String groomService = sc.nextLine(); 
                   dog.setGroomService(groomService); 
                   System.out.print("Groom price: ");
                   float groomPrice = sc.nextFloat();
                   dog.setGroomCost(groomPrice);
                   sc.nextLine();
                   System.out.println("");
                   
                   System.out.print("Is " + firstName + " participating in daycare?(yes/no): ");
                   String daycareService = sc.nextLine();
                   if (daycareService.equals("yes")){
                        dog.setDaycareService(daycareService);
                        System.out.print("Daycare cost: ");
                        float daycareCost = sc.nextFloat(); 
                        dog.setCostDaycare(daycareCost);
                        sc.nextLine();
                        System.out.println("");
                        System.out.println(dog.dogBasicInfo());
                        System.out.println(dog.dogInfo());
                    }
                }
            }
        }
        else if (newDog.equals("no")){
            tenure dog = new tenure();
            System.out.println("Dog's First Name: ");
            String firstName = sc.nextLine();
            dog.setFirstname(firstName);
            System.out.println("Dog's Last Name: ");
            String lastName = sc.nextLine();
            dog.setLastname(lastName); 
            System.out.println("Dog's breed: ");
            String breed = sc.nextLine();
            dog.setdogBreed(breed);
     
            //dog info if staying 
            System.out.print("Is " + firstName + " " + lastName + " here for a service?(yes/no):  "); 
            String hereForService = sc.nextLine(); 
            if (hereForService.equals("yes")){
                System.out.print(firstName + "'s cubby number: ");
                int cubby = sc.nextInt();
                dog.setCubby(cubby);
                sc.nextLine();
                System.out.print("Arrival date: ");
                String arrival = sc.nextLine();
                dog.setArrival(arrival);
                System.out.print("Departure date: "); 
                String departure  = sc.nextLine();
                dog.setDeparture(departure); 
                System.out.println("Time out: "); 
                String timeOut = sc.nextLine(); 
                dog.setTimeout(timeOut);
                System.out.println("Is " + firstName + " " + lastName + " here for Boarding, Grooming, Daycare: "); 
                String service = sc.nextLine(); 
                if (service.equals("boarding")){
                    dog.setBoardingService(service);
                    //ENTER THE PRICE FOR THE BOARDING (DEPARTURE DATE-ARRIVAL DATE
             
                    System.out.println("Is " + firstName + " being groomed?(yes/no): "); 
                    String groom = sc.nextLine(); 
                    if (groom.equals("yes")){
                        System.out.print("What groom Service(s): ");
                        String groomService = sc.nextLine(); 
                        dog.setGroomService(groomService); 
                        System.out.print("Groom price: ");
                        float groomPrice = sc.nextFloat();
                        dog.setGroomCost(groomPrice);
                        sc.nextLine();
                        System.out.println("");
                        System.out.println(dog.dogBasicInfo());
                        System.out.println(dog.dogInfo());
                        }
            }
                else if (service.equals("daycare")){
                    dog.setDaycareService(service);
                    System.out.print("Daycare cost: ");
                    float daycareCost = sc.nextFloat(); 
                    dog.setCostDaycare(daycareCost); 
                    sc.nextLine();
                    System.out.println("");
                    System.out.println(dog.dogBasicInfo());
                    System.out.println(dog.dogInfo());
                    }
                
                else if(service.equals("grooming")){
                    dog.setGroomService(service);
                    System.out.print("What groom Service(s): ");
                    String groomService = sc.nextLine(); 
                    dog.setGroomService(groomService); 
                    System.out.print("Groom price: ");
                    float groomPrice = sc.nextFloat();
                    dog.setGroomCost(groomPrice);
                    sc.nextLine();
                 
                    System.out.print("Is " + firstName + " participating in daycare?(yes/no): ");
                    String daycareService = sc.nextLine();
                    if (daycareService.equals("yes")){
                        dog.setDaycareService(daycareService);
                        System.out.print("Daycare cost: ");
                        float daycareCost = sc.nextFloat(); 
                        dog.setCostDaycare(daycareCost);
                        sc.nextLine();
                        System.out.println("");
                        System.out.println(dog.dogBasicInfo());
                        System.out.println(dog.dogInfo());
                        
                }
            }
        }
        
        }
    }
}

      
            
             
  