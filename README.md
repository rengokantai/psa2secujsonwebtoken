# psa2secujsonwebtoken


## 6. Use JSON Web Tokens to Secure Web API Methods
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

