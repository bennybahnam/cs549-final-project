# Malicious URL Dectection Dataset Preprocessing

This folder contains all the necessary code to feature engineer URL datasets containing malicious and legitimate URLs. It processes the URLs as the following:

1. Drop exact duplicates in the dataset
2. Attempt to pull more data to achieve a 50-50 split if necessary
3. Ensure all entries are in lowercase
4. Extract and append the following information:
    1. Scheme
    2. Subdomain
    3. Registrable domain
    4. Suffix
    5. Path
    6. Query
    7. Fragment
    8. Port
    9. Username
    10. Password
    11. Host
5. Flag http and https entries
6. Count and append the following lengths:  
    a. Total length  
    b. Host length  
    c. Path length  
    d. Query length  
    e. Fragment length
7. Count and append the counts the following characters:  
    a. Dots  
    b. Slashes  
    c. Other special characters (ie -, _, %, @, ?, =, &)  
    d. Digits  
8. Calculate and append the Shannon entropy of the entries
9. Flag the following keywords  
    a. Login  
    b. Verify  
    c. Update  
    d. Secure  
    e. Account  
    f. Bank  
    g. Paypal  
    h. Free  
    i. Prize  
    j. Gift  
    k. Confirm  
    l. Win  
    m. Signin  
    n. Support 
    10. Flag link shorteners
    11. Flag domains that are purely numbers

To run the script, simply run all the cells. It saves the dataset in the root of the workspace, acessible for all models to import and use.