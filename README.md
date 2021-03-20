# MyRPC

> Author：ZiKang Deng
>  
> Date：2021-03-20

- ## Introduction
```markdown
This is my own protocol for RPC.It is based on HTTP and encoded in Base64.
``` 

- ## Protocol
```markdown
Client:
{
	"Token":"token string",
	"Function name":"Function name",
	"Input parameter":{
		XXXX
	}
}

e.g.:
{
	"Token":"abcdefg12346789",
	"Function name":"AddTowNum",
	"Input":{
		"one":"1",
		"tow":"10"
	}
}

Base64Enc:ewoJIlRva2VuIjogImFiY2RlZmcxMjM0Njc4OSIsCgkiRnVuY3Rpb24gbmFtZSI6ICJBZGRUb3dOdW0iLAoJIklucHV0IjogewoJCSJvbmUiOiAiMSIsCgkJInRvdyI6ICIxMCIKCX0KfQ==

Server:
{
	"Status":"Status code",
	"Message:"Message string", 
	"Output":{
		XXXX
	}
}

e.g.:
{
	"Status":"0",
	"Message:"Execute successfully", 
	"Output":{
		"result":"11"
	}
}

Base64Enc:ewoJIlN0YXR1cyI6IjAiLAoJIk1lc3NhZ2U6IkV4ZWN1dGUgc3VjY2Vzc2Z1bGx5IiwgCgkiT3V0cHV0Ijp7CgkJInJlc3VsdCI6IjExIgoJfQp9
``` 