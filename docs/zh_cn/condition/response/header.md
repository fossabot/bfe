# Response header相关的条件原语

- **res_header_key_in(patterns)**
  - 判断响应头部中key是否满足patterns之一
  
  - patterns，字符串，表示多个可匹配的pattern，用‘|’连接
  
    ```
    # 头部中key为Header-Test的响应
    res_header_key_in(“Header-Test”)
    ```
- **res_header_value_in(key, patterns, case_insensitive)**
  
  - 判断header中key对应的值是否满足patterns之一
  
  - key，字符串
  
  - patterns，字符串，表示多个可匹配的pattern，用‘|’连接
  
  - case_insensitive，bool类型，是否忽略key的值大小写
  
    ```
    # 头部中，key为Header-Test的值为XXX的响应
    res_header_value_in("Header-Test", "XXX", true)
    ```
  
    
