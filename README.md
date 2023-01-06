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
	![image](https://user-images.githubusercontent.com/106193347/211063898-a558dcb9-d736-4f3d-a2b5-2eea4557ad83.png)

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

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

### ADD ENTITY
 (precisa de body e de token - referenciar o id do user dentro do body conforme abaixo:)
 
baseUrl/users/{id do user}
+
BODY:
		{
		"cpfCnpj": "",
		"nomeRazao": "",
		"apelidoFantasia" : "",
		"tipo": "",
		"insEstadual":"",
		"insMunicipal":"",
		"cep":"",
		"rua":"",
		"numero":"",
		"complemento":"",
		"bairro":"",
		"cidade":"",
		"telefone":"",
		"celular":"",
		"email":"",
		"site":"",
		"userId": {Insira o ID do user AQUI}
	}
	
 :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

### GET INDIVIDUAL ENTITY
 (sem body e precisa de token)
 
 baseUrl/entities?id={id da entidade cadastrada}
 
 :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
 
### GET ALL ENTITIES
 (sem body e precisa de token)
 
 baseUrl/entities
 
 :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
 
 ### EDIT ENTITY
 (precisa de body e precisa de token - referenciar userId no body conforme abaixo)
 
 baseUrl/entities/{id da entidade a ser editada}
 +
	{
		"cpfCnpj": "09810874936",
		"nomeRazao": "Ampoula de ourddo",
		"apelidoFantasia" : "",
		"tipo": "",
		"insEstadual":"",
		"insMunicipal":"",
		"cep":"",
		"rua":"",
		"numero":"",
		"complemento":"",
		"bairro":"",
		"cidade":"",
		"telefone":"",
		"celular":"",
		"email":"",
		"site":"",
		"userId": {INSIRA useId AQUI}
	}
 
 :::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
