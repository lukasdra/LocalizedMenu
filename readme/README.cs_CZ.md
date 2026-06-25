# LocalizedMenu
Lokalizační nástroj a lokalizovaná nabídka(menu) pro uživatele Sublime Text 2/3/4

- Nabízí jednoduchou cestu k přidání nového jazyka
- Podporuje více verzí
- Podporuje sdílené nabdky
- Automatické záloky lokálních nabídek
- Automatické rozbalení nových sestavení v angličtině

# README.md
- cs_CZ [Czech](readme/README.cs_CZ.md)
- de_DE [Deutsch](readme/README.de_DE.md)
- en [English](README.md)
- es_ES [Español](readme/README.es_ES.md)
- fr_FR [Français](readme/README.fr_FR.md)
- hu [Magyar](readme/README.hu.md)
- hy [Հայերեն](readme/README.hy.md)
- pt_BR [Português do Brasil](readme/README.pt_BR.md)
- ru [Русский](readme/README.ru.md)
- sv_SE [Svenska](readme/README.sv_SE.md)
- zh_CN [简体中文](readme/README.zh_CN.md)
- zh_TW [繁体中文](readme/README.zh_TW.md)

# Tento projekt je také hostován na
- [GitHub](https://github.com/zam1024t/LocalizedMenu)
- [Gitee](https://gitee.com/zam1024t/LocalizedMenu)

# Ve zkratce
#### Běží na Windows
![Běží na Windows](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_win.gif)
#### Běží na OS X
![Běží na OS X](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_osx.gif)
#### Běží na Ubuntu
![Běží na Ubuntu](https://raw.githubusercontent.com/zam1024t/LocalizedMenu/shots/shots/LocalizedMenu_linux.gif)

# Instalace
- S kontrolou balíčků
	- instaluj [Package Control](https://packagecontrol.io/installation)
	- vyhledej `LocalizedMenu`
- Manuálně
	- stáhni [master.zip](https://github.com/zam1024t/LocalizedMenu/archive/master.zip)，rozbal do `Packages`，a pak přejmenuj `LocalizedMenu-master` to `LocalizedMenu`
	- klonuj git do `Packages`
	```
	git clone https://github.com/zam1024t/LocalizedMenu
	```

# Použití
- Přepni v nabídce
	- přes `Preference` -> `Languages`
- Přepni v příkazovém panelu
	- `Ctrl+Shift+P`, napiš`lmxx`(*xx* je kód země) pro přepnutí

# Přidat jazyk
- kopíruj `locale/en/en.json` do `locale/<locale>/<locale>.json`, přelož do svého jazyka
- kopíruj `menu/<version>/en/*` do `menu/<version>/<locale>/*`, přelož do svého jazyka
- Například, přidání překladu pojmenovaného  `my` pro Sublime Text Build 3999
	- otevři adresář `LocalizedMenu`, přes `Preference` -> `Languages` -> `Add a language`
	- otevři `locale`, kopíruj `en` na `my`
	- otevři `my`, přejmenuj `en.json` na `my.json`, uprav jako:

	```JavaScript
	{
		"link": "",
		"hidden": false,
		"caption": "MyLanguage",
		"mnemonic": "m"
	}
	```

	- otevři `menu/3999`, kopíruj `en` na `my`, a přelož všechny položky `caption` v souborech nabídek
	- detekuj jazyk přes `Preference` -> `Languages` -> `Detect`, pak zobraz `MyLanguage (my)`

	> **konfigurace překladu**<br>
	> link： cílový soubor s překladem<br>
	> hidden： skrytá nabídka<br>
	> caption： jazyk<br>
	> mnemonic： klávesová zkratka，volitelná

# Přihlášení jazyka
- název překladu musí být pojmenován jako `<languageCode>` nebo `<languageCode>_<countryCode>`
	- `<languageCode>` malým písmem, `<countryCode>` velkým písmem
	- Jazyk: https://www.wikipedia.org/wiki/ISO_639-1
	- Země: https://www.wikipedia.org/wiki/ISO_3166-1
- Vytvoř fork repozitáře
- Vytvoř žádost o změny

# Jazyky a překladatelé
- cs_CZ Czech *by [lukasdra](https://github.com/lukasdra)*
- de_DE Deutsch *by [Standarduser](https://github.com/Standarduser)*
- es Español *by [Christopher](https://t.me/Azriel_7589)*
- es_ES Español *by [Dastillero](https://github.com/dap39)*
- fr_FR Français *by [fxbenard](https://github.com/fxbenard)*
- hu Magyar *by [Tamás Balog](https://github.com/picimako)*
- hy Հայերեն *by [Arman High Foundation](https://github.com/ArmanHigh)*
- pt Português do Brasil *by [JNylson](https://github.com/jnylson)*
- ru Русский *by [Dimox](http://dimox.name) & [Ant0sh](https://github.com/Ant0sh) & [Maksim Arhipov](https://github.com/OSPanel)*
- sv_SE Svenska *by [H2SO4JB](https://github.com/H2SO4JB)*
- zh_CN 简体中文 *by [Zam](https://github.com/zam1024t)*
- zh_TW 繁体中文 *by [Zam](https://github.com/zam1024t)*

# Související
- https://github.com/wbond/package_control_channel/pull/5665
- https://github.com/rexdf/ChineseLocalization/issues/10

# Licence
[The MIT License](LICENSE)
