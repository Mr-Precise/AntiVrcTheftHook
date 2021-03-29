# Anti VRChat theft discord token and vrc password

**English version** [**HERE**](README_EN.md)

*Для Русскоязычных пользователей:*

На некоторых серверах Discord распостраняются вредоносные .unitypackage пакеты c аватарами шейдерами и подобным от "плохих" людей.

- **Как определить наличие этого кода:**

Распаковать пакет, проверить наличие файлов и данных строк кода:

По пути `Assets\DynamicBone\Scripts\DynamicBone.cs`

![2](https://user-images.githubusercontent.com/3824793/111828286-60f08680-88eb-11eb-8140-58f209a5dfc4.png)
строка 148 содержит подобные строки: <u>WebClient</u>, <u>webClient.DownloadString, Encoding.UTF8.GetString(Convert.FromBase64String</u>, <u>aHR0cHM6Ly9wb2l5b21pLnRrL2xvZ2luLw==</u>

По пути `Assets\DynamicBone\Scripts\DynamicBoneSquareCollider.cs`

![1](https://user-images.githubusercontent.com/3824793/111828049-02c3a380-88eb-11eb-80b8-75dd593dd775.png)

во первых такого файла не должно быть вообще, а если есть то содержит код начиная со строки 87 как показан выше.
Может быть вшит в якобы улучшенный VRCSDK.

- **Что оно делает?**

Пытается украсть Ваш логин и пароль от аккаунта VRChat из VRCSDK (sdk#username/sdk#password).

Пытается украсть Ваш Discord Token - о вашей переписке узнает кто-то еще.
Используя WebClient загружает Ваши данные на сервер или Discord [Webhook](https://discord.com/developers/docs/resources/webhook) злоумышленника.

- **Как противодействовать?**

Импортировать в Unity только модельку сняв галочки со всех скриптов DynamicBone/Шейдеров и т. д. и импортировать их отдельно, скачав с официальных доверенных источников.
По возможности заблокировать доменное имя poiyomi.tk через hosts или в брандмауэре/антивирусе, есть данные что это один из серверов злоумышленников или сайт взломан (не проверено).

И да, бесплатный сыр бывает только в мышеловке.
В раздачах "платных моделек" для VRChat может быть что угодно.
Будьте внимательны.

- Так же **рекомендую** прочитать [Часто задаваемые вопросы](FAQ.md)
