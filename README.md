# fastapi-simple-oauth2-front-end
A super simple HTML/JQuery front-end for FastAPI OAuth2 tutorial example.

This "main.py" file is from the OAuth2 tutorial at:
https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/
or if it is the distant future, here:
https://web.archive.org/web/20230127160400/https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/

The only tweak I've made was to add this bit:

```python
app.add_middleware(
    CORSMiddleware,
    allow_origins=["*"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)
```
... in order to prevent cross-origin/CORS error.


## How To Run This
1) Install uvicorn.
2) In the directory of this "main.py" file, run "uvicorn main:app --reload" in the terminal.
3) (If you run uvicorn on a different port, don't forget to tweak the "server" variable in the "script.js" file.)
4) Open the "index.html" file in your browser ( CTRL+o in most browsers )
5) If everything worked you should see a login page. For a successful login, try user: "johndoe" pass: "secret"
