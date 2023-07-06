# Disney-Checker

🎌 - Simple disney checker no ratelimite with auth req

i made this for myself at first, but now that i am making a new github i'm willing to share it

![image](https://github.com/capabl1/Geoguessr-request-hack/assets/137743238/7ce323af-82b8-45bc-baf5-8ed26a368d6f)
- Fetch all the registered email on Disney plus based on a email list ( txt file )
  
``` 
[GET] https://disney.api.edge.bamgrid.com/v1/public/graphql
```

![image](https://github.com/capabl1/disney-checker/assets/137472232/59ff66f6-782a-43f0-8670-6b3080bb4fed)


https://cdn.discordapp.com/attachments/1107003739526660168/1107107866617331752/2023-05-13_20-50-33.mp4



> function that extracts and returns THE authorization token from THE request's headers SINCE it is expiring every 1 hour ( or maybe + ), removing the "Bearer " prefix if present for a correct string, you can try first with getting it manually

```JS
const auth = (request) => {
  const authorizationHeader = request.headers['authorization'];
  const authorizationToken = authorizationHeader ? authorizationHeader.replace(/^Bearer /, '') : '';
  return authorizationToken;
};
```




| Name     | Headers |
| ---      | ---       |
| Accept                  | application/json                                |
| Accept-Encoding         | gzip, deflate, br                               |
| Accept-Language         | fr-FR,fr;q=0.9,en-US;q=0.8,en;q=0.7             |
| authorization           | ( explained  )                                  |
| Content-Type            | application/json                                |
| Connection              | keep-alive                                      |
| Host                    | disney.api.edge.bamgrid.com                     |
| Origin                  | https://www.disneyplus.com                      |
| Referer                 | https://www.disneyplus.com/                     |
| Sec-Ch-Ua               | "Google Chrome";v="111", "Not(A:Brand";v="8", "Chromium";v="111" |
| Sec-Ch-Ua-Mobile        | ?0                                              |
| Sec-Ch-Ua-Platform      | "Windows"                                       |
| Sec-Fetch-Dest          | empty                                           |
| Sec-Fetch-Mode          | cors                                            |
| Sec-Fetch-Site          | cross-site                                      |
| User-Agent              | Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/111.0.0.0 Safari/537.36 |
| X-Application-Version   | 1.1.2                                           |
| X-Bamsdk-Client-Id      | disney-svod-3d9324fc                            |
| X-Bamsdk-Platform       | javascript/windows/chrome                       |
| X-Bamsdk-Platform-Id    | browser                                         |
| X-Bamsdk-Version        | 22.1                                            |
| X-Dss-Edge-Accept       | vnd.dss.edge+json; version=2                    |
| X-Request-Id            | 857325bc-a6b5-4561-90ee-190596333826            |




Made with 🫀 by kAzen ( capabl1 )
