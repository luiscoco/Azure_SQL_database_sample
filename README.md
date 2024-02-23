# Azure SQL database sample

We first have to log in to Azure Portal

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/a7b80f6e-c4b5-4768-8497-e21e9f22ddcf)

We navigate into Create a new Resource and we select **Azure SQL**

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/935ed12c-7321-4bed-adbb-5e777f173367)

We select the option **SQL databases** create

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/0b7f0cba-42c0-478e-8024-c24a352a4718)

We select the button **Apply offer (preview)**

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/8ab2cef5-c7c0-4826-b890-3f016ec4c80d)

We input the requested data to create the database: : Subscription, ResourceGroup, Databasename

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/676b0469-fee2-4b6d-a561-1ce45a84a38a)

We also have to create a new Server. We input the Server name and location

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/bb7552ff-b173-452d-994a-2a6739c33630)

We also select the **Use SQL authentication** option, and input the login name and password

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/0de6d222-fdef-4d60-9367-6e6efdcb3acc)

We also have to configure the database computing resources

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/d9c97754-fa36-4228-8999-e8b58781c817)

We input the required vCores and storing menory size

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/29490aa4-541a-4550-8daa-21c52b899605)

We also input the replication option and the behaviour when free offer finish

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/13c8417d-6f1f-4352-9fcc-45ff147f967a)

We also have to select the Networking options

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/89b3ada5-4106-4d15-bf6e-d36851ae1fd2)

We finally create the database

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/f0ad0927-fec4-4161-9ede-ad6d5021c898)

We go to the resource

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/3c5a0dfb-d8c0-4dac-a349-79a8922732ce)

And then we copy the database connection string and input this value in the **appsettings.json** file

```
Server=tcp:myidentityserver.database.windows.net,1433;Initial Catalog=DotNet8Authentication;Persist Security Info=False;User ID=admin123;Password={your_password};MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
```

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/16922b1a-ae0e-41e9-bc2b-c62836d225c4)

**IMPORTANT NOTE**: do not to forget to replace your password in the above connectionstring

we replace **{your_password}** with **Luiscoco123456**

This is the final connection string

```
Server=tcp:myidentityserver.database.windows.net,1433;Initial Catalog=DotNet8Authentication;Persist Security Info=False;User ID=admin123;Password=Luiscoco123456;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
```

We also have to **Configure network access** to your SQL server

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/515f31f3-f634-471c-9c70-750e615a1a48)

We add our local laptop IP address in the firewall rules

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/c267c8fd-ec8f-48e2-94ad-11d2ee31d2c3)

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/cb71ab21-e348-4169-80be-554ba22b80a5)

We run SSMS and check the Azure SQL database is working fine

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/9aef64d9-bf89-4228-98e9-57fb9d133d41)

We input the password **Luiscoco123456** we input when creating the Server

We confirm the connection is ok

![image](https://github.com/luiscoco/Identity_dotNET8_Authentication/assets/32194879/bd4b7b59-6945-45e1-af9e-5cb2997c9948)



