# dnacenter_queries
Use powershell to query Cisco DNA Center / Catalyst Center
##  ===================================================================
##  Script creator: wils0h
##
##  Last edited 01/28/2024
##  Version 1.0.0
##  ================= README ==========================================
##  This is a Powershell script that queries Cisco DNA Center for all
##  Catalyst 9410 switches, pulls the serial numbers of the modules in
##  each Catalyst 9410 switch, and filters the output for a specific
##  line card part number and for serial numbers that contain certain
##  characters.
##  REQUIRES PS 7 FOR THE "INVOKE-RESTMETHOD" -CREDENTIAL" OPTION.
##  *** SPECIAL API FUNCTIONS *****************************************
##  The API requires the credentials of a DNAC user. A special user was
##  created with limited permissions (OBSERVER-ROLE) to prevent
##  unintended consequences.
##  
##  The API authentication works by validating credentials passed to
##  the authentication API function and then responds with an API token
##  that is valid for 1 hour. This API token is then what is used to
##  authenticate subsequent API calls.
##  This is different than some other APIs that generate a token in a
##  different manner and that token may not have an expiration.
##  *******************************************************************
##  This can be used as a template for future DNAC queries.
##  ===================================================================
