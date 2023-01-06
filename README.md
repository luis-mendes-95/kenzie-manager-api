# Kenzie Manager - API

Essa é a API do projeto Kenzie Manager.

## Base URL

https://kenzie-manager-api.onrender.com


### Como manipular os dados:

### :::::::::::::::::Users (Usuários) 

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

### CADASTRAR USUÁRIO
(Utiliza body, não precisa de token)

baseUrl/register
+
BODY:
	{
		"email": "useremail@mail.com",
		"password": "senhaSENHA123@",
		"name": "João Dono"	
	}
	
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
	
### LOGIN
(Utiliza body, não precisa de token)

baseUrl/login
+
BODY:
	{
		"email": "useremail@mail.com",
		"password": "senhaSENHA123@"
	}
	
:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
	
### DELETE USER
(sem body, precisa de token)

baseUrl/users/{id do user}

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

### EDIT USER
(Utiliza body e precisa de token)

baseUrl/users/{id do user}
+
BODY:
	{
		"email": "useremail@mail.com",
		"password": "senhaSENHA123@",
		"name": "João Dono"
	}

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

### GET USER
 (sem body e precisa de token)
 
 baseUrl/users/{id do user}
 
 :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
 
 
### :::::::::::::::::Entities (CPF / CNPJ) 

