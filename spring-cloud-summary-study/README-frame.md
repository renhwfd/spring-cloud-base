# spring-cloud-summary-study
架构图
```text
                                  +---------+                                     
                                  |  客户端  |                                       
                                  |  client |                                     
                                  +---------+                                     
                                       |                                          
                                       V                                          
                                  +---------+                                     
                                  | gateway-|                                     
                                  | service |                                     
                                  +---------+                                     
                                       |                                          
                        +--------------|--------------+                           
                        V              V              V                           
                 ..............................................                   
  +---------+    .  +---------+    +---------+    +---------+ .    +---------+    
  | zipkin- |<---.  |  user-  |    |  blog-  |    |  uaa-   | .--->| turbine |    
  | service |    .  | service |    | service |    | service | .    |         |    
  +---------+    .  +---------+    +---------+    +---------+ .    +---------+    
                 ..............................................         |         
                        A                |           |                  |         
                        |                |           |                  |         
                        |                V           V                  V         
  +---------+       +---------+    +---------+    +---------+      +---------+    
  |   git   |------>| config- |    | eureka- |    |  log-   |      |  admin- |    
  |         |       | service |    | server  |    | service |      | service |    
  +---------+       +---------+    +---------+    +---------+      +---------+    
..................................................................................
                                     |                   A                        
                                     |                   |                        
                                     V                   V                        
                                +---------+          +---------+                  
                                |  mysql  |          | RabbitMq|                  
                                |         |          |         |                  
                                +---------+          +---------+                  
```