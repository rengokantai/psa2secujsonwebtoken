# psa2secujsonwebtoken


## 6. Use JSON Web Tokens to Secure Web API Methods
### 2 Add Authorize Attribute
```
using System.tas
using Microsoft.AspNetCore.Mvc;
using Micorsoft.AspNetCore.Http;
using Microsoft.AspNetCore.Authorization;
using PtcApi.Model;
namespace PtcApi.Controllers {
  [Route("api/[controller]")]
  public class ProductController: BaseApiController
  {
    [HttpGet]
    [Authorize]
    public IActionResult Get()
    {
      IActionResult ret = null;
      List<Product> list = new List<Product>();
    }
  }
}
```

### 3 Add JWT Packages to Web API Project
```
dotnet add package System.IdentityModel.Token.Jwt
dotnet add package.Microsoft.AspNetCore.Authentication.JwtBearer"Jwt
```

### 5 Add Settings to JSON File and Read the Settings
```
public JwtSettings GetJwtSettings(){
  JwtSettings settings = new JwtSettings();
  settings.Key = Configuration["JwtSettings:key"];
  settings.Audience = Configuration["JwtSettings:audience"]'
  return settings;
}
```


### 6 How to Setup Authentication in the Web API Project

