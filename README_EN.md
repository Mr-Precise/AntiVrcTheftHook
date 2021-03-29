# Anti VRChat theft discord token and vrc password

**Russian version** [**HERE**](README.md)

*English version:*

On some servers Discord distribute malicious .unitypackage packets with avatars, shaders and the like from "bad" people.

- **How to determine the presence of this code:**

Unpack the package, check the availability of files and these lines of code:

On path: `Assets\DynamicBone\Scripts\DynamicBone.cs`

![2](https://user-images.githubusercontent.com/3824793/111828286-60f08680-88eb-11eb-8140-58f209a5dfc4.png)
string 148 contains: <u>WebClient</u>, <u>webClient.DownloadString, Encoding.UTF8.GetString(Convert.FromBase64String</u>, <u>aHR0cHM6Ly9wb2l5b21pLnRrL2xvZ2luLw==</u>

On path: `Assets\DynamicBone\Scripts\DynamicBoneSquareCollider.cs`

![1](https://user-images.githubusercontent.com/3824793/111828049-02c3a380-88eb-11eb-80b8-75dd593dd775.png)

First, there shouldn't be such a file. And if exists, then line 87 contains: as above.
May be added to the supposedly improved VRCSDK.

- **What does it do?**

It is trying to steal your username and password from the account of VRChat VRCSDK (sdk#username/sdk#password).

It is trying to steal your Discord Token - your privacy will be at risk.
Using WebClient uploads your data to the server or Discord [Webhook](https://discord.com/developers/docs/resources/webhook) of the attacker.

- **How to protect?**

Import only model into Unity by unchecking all scripts DynamicBone/Shaders etc and import them separately, downloading from official trusted sources.
If possible, block the poiyomi.tk domain name on hosts file or in firewall / antivirus, There is evidence that this is one of the attackers' servers or the site has been hacked (not verified).

Free is risky, you were warned :)
In the giveaway "purchased models" for VRChat could be anything.
Be careful.

- I also **recommend** reading [Frequently asked Questions(FAQ)](FAQ_EN.md)
