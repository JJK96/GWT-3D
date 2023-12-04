GWT-3D
======

GWT-3D is a tool aimed at helping you during penetration testing on GWT technology. For a full description see http://miaouplop.github.io/GWT-3D/.  
This program is intended to be pushed to the original repository (https://github.com/GDSSecurity/GWT-Penetration-Testing-Toolset) once enough 
testing have been completed.

== Examples

```
$ python gwt3d.py decode -i '7|0|9|https://example.com/api|0FAADF1A5E9D0D68E7B402F07F8D7168|com.example.services.UserService|update|java.lang.Boolean/476441737|com.example.UserDTO|java.lang.String|John|Doe|1|2|3|4|2|6|5|2|8|9|1|' -j | jq
{
  "class": "com.example.services.UserService",
  "method": "update",
  "nb": 2,
  "params": [
    {
      "typename": "com.example.UserDTO",
      "values": [
        "John",
        "Doe"
      ],
      "flag": false,
      "is_custom_obj": true,
      "is_list": false,
      "is_array": false
    },
    {
      "typename": "java.lang.Boolean/476441737",
      "values": [
        "true"
      ],
      "flag": false,
      "is_custom_obj": false,
      "is_list": false,
      "is_array": false
    }
  ]
}
```
