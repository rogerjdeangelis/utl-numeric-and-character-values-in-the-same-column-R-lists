# utl-numeric-and-character-values-in-the-same-column-R-lists
Sum just the numeric values in a column that contains both numeric and character values 
    Problem: Sum just the numeric values in a column that contains both numeric and character values                            
                                                                                                                                
    SAS datastep does not support mixed type in the same column but R and Python do.                                            
                                                                                                                                
    github                                                                                                                      
    https://tinyurl.com/y3gdxonq                                                                                                
    https://github.com/rogerjdeangelis/utl-numeric-and-character-values-in-the-same-column-R-lists                              
                                                                                                                                
    Double edged sword!!                                                                                                        
    I wish packages would not produce output objects with complex list structures.                                              
    Dataframes inside dataframes with mixed types at different nestings.                                                        
                                                                                                                                
    SAS Forum                                                                                                                   
    https://tinyurl.com/y5stmq8j                                                                                                
    https://communities.sas.com/t5/New-SAS-User/Input-Column-that-can-have-both-character-amp-number-but-should/m-p/566102      
                                                                                                                                
    *_                   _                                                                                                      
    (_)_ __  _ __  _   _| |_                                                                                                    
    | | '_ \| '_ \| | | | __|                                                                                                   
    | | | | | |_) | |_| | |_                                                                                                    
    |_|_| |_| .__/ \__,_|\__|                                                                                                   
            |_|                                                                                                                 
    ;                                                                                                                           
                                                                                                                                
    R dataframe ( like a SAS dataset)                                                                                           
                                                                                                                                
            X    Y                                                                                                              
                                                                                                                                
       1    1    a   * type = character                                                                                         
       2    2    1   * type = numeric                                                                                           
       3    3    2                                                                                                              
       4    4    3                                                                                                              
       5    5    b                                                                                                              
                                                                                                                                
    CONTENTS                                                                                                                    
                                                                                                                                
    'data.frame':   5 obs. of  2 variables:                                                                                     
                                                                                                                                
     $ x: int  1 2 3 4 5                                                                                                        
     $ y:List of 5                                                                                                              
      ..$ : chr "a"                                                                                                             
      ..$ : num 1                                                                                                               
      ..$ : num 2                                                                                                               
      ..$ : num 3                                                                                                               
      ..$ : chr "b"                                                                                                             
                                                                                                                                
    *           _                                                                                                               
     _ __ _   _| | ___                                                                                                          
    | '__| | | | |/ _ \                                                                                                         
    | |  | |_| | |  __/                                                                                                         
    |_|   \__,_|_|\___|                                                                                                         
                                                                                                                                
    ;                                                                                                                           
                                                                                                                                
    Sum the numeric values in column Y                                                                                          
                                                                                                                                
    *            _               _                                                                                              
      ___  _   _| |_ _ __  _   _| |_                                                                                            
     / _ \| | | | __| '_ \| | | | __|                                                                                           
    | (_) | |_| | |_| |_) | |_| | |_                                                                                            
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                           
                    |_|                                                                                                         
    ;                                                                                                                           
                                                                                                                                
    Sum 1 + 2 + 3 =6                                                                                                            
                                                                                                                                
    [1] 6                                                                                                                       
                                                                                                                                
    *                                                                                                                           
     _ __  _ __ ___   ___ ___  ___ ___                                                                                          
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                                         
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                         
    | .__/|_|  \___/ \___\___||___/___/                                                                                         
    |_|                                                                                                                         
    ;                                                                                                                           
                                                                                                                                
    %utl_submit_r64('                                                                                                           
    d <- data.frame(x = 1:5);                                                                                                   
    d$y <- list("a",1,2,3,"b");                                                                                                 
    d;                                                                                                                          
    str(d);                                                                                                                     
    d$y[[2]] + d$y[[3]] + d$y[[4]];                                                                                             
    ');                                                                                                                         
                                                                                                                                
    *_                                                                                                                          
    | | ___   __ _                                                                                                              
    | |/ _ \ / _` |                                                                                                             
    | | (_) | (_| |                                                                                                             
    |_|\___/ \__, |                                                                                                             
             |___/                                                                                                              
    ;                                                                                                                           
                                                                                                                                
    > d <- data.frame(x = 1:5);d$y <- list("a",1,2,3,"b");d;str(d);d$y[[2]] + d$y[[3]] + d$y[[4]];                              
                                                                                                                                
      x y                                                                                                                       
    1 1 a                                                                                                                       
    2 2 1                                                                                                                       
    3 3 2                                                                                                                       
    4 4 3                                                                                                                       
    5 5 b                                                                                                                       
                                                                                                                                
    'data.frame':	5 obs. of  2 variables:                                                                                       
     $ x: int  1 2 3 4 5                                                                                                        
     $ y:List of 5                                                                                                              
      ..$ : chr "a"                                                                                                             
      ..$ : num 1                                                                                                               
      ..$ : num 2                                                                                                               
      ..$ : num 3                                                                                                               
      ..$ : chr "b"                                                                                                             
                                                                                                                                
    [1] 6                                                                                                                       
                                                                                                                                
    >                                                                                                                           
                                                                                                                                
