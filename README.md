# writeup_securityvalley
writeup
**url: https://ctf.securityvalley.org/dashboard**
----------------------------------------------------

**NetWork**

- The shark

![image](https://user-images.githubusercontent.com/121002781/215330956-e92d8ac3-ae08-4747-8d95-34b254bfe6d2.png)

Open the file in wireshark and view it in Protocal Hirarchy.

![image](https://user-images.githubusercontent.com/121002781/215331768-232ab449-2fbc-4f24-b02e-79e1aedbcc16.png)

Suspicious http protocol. I will choose to see

I can try it in the TCP Stream.

![image](https://user-images.githubusercontent.com/121002781/215332309-e897839b-b233-41b2-892a-c5aa9ce49bb1.png)

![image](https://user-images.githubusercontent.com/121002781/215332542-98c9ce46-564f-4d52-afb0-d34bd1af1738.png)

flag: SecVal{845Ic4u7h_i5_5UP3R_5hI7}

----------------------------------------------------

- The shell

![image](https://user-images.githubusercontent.com/121002781/215332601-81acb231-12d0-4c38-893d-5acdcd346271.png)

Open the file in wireshark and view it in Protocal Hirarchy.

![image](https://user-images.githubusercontent.com/121002781/215332713-eea47371-11e8-46f6-8f02-caf668426507.png)

I would choose to look at the tcp protocol.

I can try it in the TCP Stream.

![image](https://user-images.githubusercontent.com/121002781/215332817-466c59a9-9c75-43c4-8ba2-04ea784e10f9.png)

flag: SecVal{rev_shell_fun_insec}

----------------------------------------------------

- The data

![image](https://user-images.githubusercontent.com/121002781/215332939-92a4ddaa-ef1b-494a-8e61-409f87b3bea7.png)

Open the file in wireshark and view it in Protocal Hirarchy.

![image](https://user-images.githubusercontent.com/121002781/215333335-5fe97766-c21c-4cfc-bded-0682c800bd8d.png)

Suspicious http protocol. I will choose to see

I can try it in the TCP Stream.

![image](https://user-images.githubusercontent.com/121002781/215333384-aa49f510-0618-42f1-8214-a4c413118e03.png)

I found file png, will select data as raw.

![image](https://user-images.githubusercontent.com/121002781/215333457-e10ab401-d566-472e-b121-71e5622693e5.png)

![image](https://user-images.githubusercontent.com/121002781/215334012-9aa9466f-276f-49e9-b432-cc1aa5258082.png)

flag: SecVal{g1mp_g1mp_g1mp}

----------------------------------------------------

- Malicious traffic

![image](https://user-images.githubusercontent.com/121002781/215334077-eab24111-8d01-4b58-bf8c-c036d35c4d1d.png)

Here we get the key is "bad"

Open the file in wireshark and view it in Protocal Hirarchy.

![image](https://user-images.githubusercontent.com/121002781/215334236-ff6fc737-bd15-494a-83e2-355b40bae31c.png)

Suspicious udp protocol. I will choose to see

I can try it in the UDP Stream.

![image](https://user-images.githubusercontent.com/121002781/215334450-84c7b635-514d-4455-8c4b-bcf8f18ab853.png)

In the 3rd stream, I found an encrypted message.

![image](https://user-images.githubusercontent.com/121002781/215334568-4d15cd3a-5a69-4841-b3d5-eab4e5f57ee0.png)

I tried decoding with base64 and followed by xor and key is bad

Now let's try to collect the encrypted message.

![image](https://user-images.githubusercontent.com/121002781/215334747-6d97bcdc-21fe-4056-be56-861ca2fdc443.png)

flag: SecVal{MOCKING_BIRD}

----------------------------------------------------


