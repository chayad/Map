# Map
package map;


public class Map {
    
    Coordinate C = new Coordinate();
     
     public void sfindlocation(float latitude,float longitude)
     {
         if (latitude==239.99999f && longitude==233.12222f)
         {
             System.out.println("location is US");
         }
         else if(latitude==38.786f && longitude==46.453f)
         {
             System.out.println(" location is Africa");
         }
         else if(latitude==38.786f && longitude==46.453f)
         {
             System.out.println("location is poland");
         }
         else if(latitude==108.623f && longitude==112.443f)
         {
             System.out.println("location is Japan");
         }
         else if(latitude==138.786f && longitude==46.453f)
         {
             System.out.println("location is Brooklyn");
         }
     }
  }

public class Distance {
    
    private float fdistance;

    
    public float getFdistance() {
        return fdistance;
    }

    
    public void setFdistance(float fdistance) {
        this.fdistance = fdistance;
    }
   
       public  double distance(double lat1, double lon1, double lat2, double lon2) {

  double theta = lon1 - lon2;

  double dist = Math.sin(deg2rad(lat1)) * Math.sin(deg2rad(lat2)) + Math.cos(deg2rad(lat1)) * Math.cos(deg2rad(lat2)) * Math.cos(deg2rad(theta));

  dist = Math.acos(dist);

  dist = rad2deg(dist);

  dist = dist * 60 * 1.1515;


  return (dist);

}

public double deg2rad(double deg) {

  return (deg * Math.PI / 180.0);

}

public double rad2deg(double rad) {

  return (rad * 180 / Math.PI);
} 

}


package map;


public class PoliticalMap {
    private int ipopulation;
    private int iLiterecy;
    private int iPerCapitalIncome;
    private String sLanguage;
    private float result=0;
    public int getIpopulation() {
        return ipopulation;
    }

    public void setIpopulation(int ipopulation) {
        this.ipopulation = ipopulation;
    }

    public int getiLiterecy() {
        return iLiterecy;
    }

    public void setiLiterecy(int iLiterecy) {
        this.iLiterecy = iLiterecy;
    }

    public int getiPerCapitalIncome() {
        return iPerCapitalIncome;
    }

    public void setiPerCapitalIncome(int iPerCapitalIncome) {
        this.iPerCapitalIncome = iPerCapitalIncome;
    }

    public String getsLanguage() {
        return sLanguage;
    }

    public void setsLanguage(String sLanguage) {
        this.sLanguage = sLanguage;
    }
    
    public void fpopDensity(float area, int pop)
    {
       
            result= pop/area;
            System.out.println("population density is"+result);
        
     }
    
}


package map;


public class GeoMap {
    private float ftemp;
    private String swealth;
    private String stypesoil;
    private float fAnualrainfall;

    
    public float getFtemp() {
        return ftemp;
    }

    
    public void setFtemp(float ftemp) {
        this.ftemp = ftemp;
    }

    
    public String getSwealth() {
        return swealth;
    }

    
    public void setSwealth(String swealth) {
        this.swealth = swealth;
    }

   
    public String getStypesoil() {
        return stypesoil;
    }

    
    public void setStypesoil(String stypesoil) {
        this.stypesoil = stypesoil;
    }

    
    public float getfAnualrainfall() {
        return fAnualrainfall;
    }

   
    public void setfAnualrainfall(float fAnualrainfall) {
        this.fAnualrainfall = fAnualrainfall;
    }
    
    
    public void TypeofCropcultivation(String soiltype)
    {
       if(soiltype=="blacksoil")
       {
           System.out.println("Type of Cropcultivation is paddy");
       }
       
       else if (soiltype=="redsoil")
       {
           System.out.println("Type of Cropcultivation is sugarcane");
       }
     
    }
    
    
}


package map;

public class main {
    
    public static void main(String args[])
    {
        Distance D = new Distance();
        GeoMap G = new GeoMap();
        PoliticalMap P = new PoliticalMap();
        Map M = new Map();
        
        G.TypeofCropcultivation("blacksoil");
        G.TypeofCropcultivation("redsoil");
        
        M.sfindlocation(239.99999f, 233.12222f);
        M.sfindlocation(38.786f, 46.453f);
        
        D.distance(34.9, 76.9, 67.9, 35.9);
        System.out.println("Distance is"+D.deg2rad(9));
        
        P.fpopDensity(190, 50000);
        
    }
}


    


