# array-bike-implentation- by nandha sir
class Bike implements Comparable<Bike>{
          int fuelCapacity;
          String name;
          double price;
          long engineNumber;
          
          Bike(int fuelCapacity,String name,double price,long engineNumber) {
               this.fuelCapacity = fuelCapacity;
               this.name = name;
               this.price = price;
               this.engineNumber = engineNumber;
          }
          
                int compareTo(Bike bike) {  
                        if(price==bike.price)  
                          return 0;  
                            else if(price>bike.price)  
                              return 1;  
                        else  
                          return -1;  
                  }  



      }
      
      class Main {
            psvm(-) {
                 Bike b1 = new Bike(9,'TVS',120000.25,878787878);
                 Bike b2 = new Bike(13,'KTM',220000.75,978787878);
                 Bike b3 = new Bike(8,'RE',190000.05,678787878);
                 Bike b4 = new Bike(14,'YAMAHA',200000.15,178787878);
                 Vector<Bike> v = 
                    new Vector<Bike>(Arrays.asList(b1,b2,b3,b4));
                 Collections.sort(v);
                 ******* Normal Iterator Common for all ********
                 Iterator<Bike> it = v.iterator();
                        while(it.hasNext()) {
                          it.next();
                          }
                 System.out.println(v);
                 ******* List Family Only **********
                 ListIterator<Bike> it = v.listIterator();  
                        while(it.hasNext()) { 
                          it.next(); 
                          }
                 System.out.println(v);
                 *********Enumeration Only for list but Vector***************
                 Enumeration<Bike> en = Collections.enumeration(v);  
                        while(en.hasMoreElements()){  
                          en.nextElement();  
                          }  
                 System.out.println(v);
                 ************************************************************
            }


       }
