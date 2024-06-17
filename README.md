https://app.powerbi.com/groups/9d405322-048d-4b2e-a547-4ae93898b0ab/reports/75a22335-29e5-43b8-b9d5-3e4d5f464320/ReportSection?experience=power-bi

   -- CHECK MOBILE FEATURES AND PRICE LIST --
   SELECT * FROM mobile_project.mobile_analysis;

    -- FIND OUT THE PRICE OF 5 MOST EXPENSIVE PHONES 
    SELECT * FROM MOBILE_ANALYSIS 
    ORDER BY PRICE DESC
    LIMIT 5;
    
     -- FIND OUT THE PRICE OF 5 MOST CHEAPEST
      SELECT * FROM MOBILE_ANALYSIS 
    ORDER BY PRICE ASC
    LIMIT 5;
    
     -- LIST OF TOP 5 SAMSUNG PHONES WITH PRICE AND ALL FEATURES
     SELECT * FROM MOBILE_ANALYSIS
     WHERE brands = "samsung" 
     ORDER BY PRICE DESC
     LIMIT 5;
     
     
     -- MUST HAVE ANDROID PHONE LIST THEN TOP 5 HIGH PRICE ANDROID PHONES
	   select * from mobile_analysis
       where operating_system_type = "android"
       order by price desc
       limit 5
     
     -- MUST HAVE ANDROID PHONE LIST THEN TOP 5 LOWER PRICE ANDROID
    
     
     
     -- MUST HAVE IOS PHONE LIST THEN TOP 5 HIGH PRICE IOS PHONE
     SELECT * FROM MOBILE_ANALYSIS
       WHERE operating_system_type = "ios"
       order by price desc
       limit 5;
       
     -- MUST HAVE IOS PHONE LIST THEN TOP 5 LOWER PRICE IOS PHONE
     SELECT * FROM MOBILE_ANALYSIS
       WHERE operating_system_type = "ios"
       order by price desc
       limit 5;
       
     -- WRITE A QUERY WHICH PHONE SUPPORT 5G AND ALSO TOP 5 PHONE WITH 5G SUPPORT
     select * from mobile_analysis
     where 5G_Availability = "yes"
     order by prize desc
     limit 5;
     
     
     -- TOTAL PRICE OF ALL MOBILE IS TO BE FOUND WITH BRAND NAME
      select sum(price),brands from mobile_analysis
      group  by brands 
      
