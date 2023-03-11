# Universal Extractor 2 _(UniExtract2)_

[![下载](https://img.shields.io/badge/download-success?style=for-the-badge)](https://github.com/Bioruebe/UniExtract2#download)

Universal Extractor 2 is a tool designed to **extract files from any type of extractable file**.

与大多数存档程序不同，UniExtract不限于.zip和.rar等标准存档。它还可以处理应用程序安装程序、磁盘映像，甚至游戏存档和其他多媒体文件。支持的文件类型概述可在https://www.legroom.net/software/uniextract 找到

本程序是【Jared Breland原创UniExtract】的非官方更新和扩展版本(http://legroom.net/software/uniextract). 由于原始版本的开发已经停止，并且多年来没有更新发布，因此出现了许多分叉（修改版本，由社区志愿者维护）。这是其中最先进的，具有一长串增强功能。

## 版本2中的新功能

- 支持500多种新文件类型
- 批处理模式
- 仅扫描模式检测任何给定文件的类型
-内置更新程序
-支持常见归档的密码列表
-改进的上下文菜单集成和状态框
-更好、更快的文件分析
-静默模式，不显示任何提示
-许多界面改进和重新设计的对话框
-资源使用/速度改进，大量错误修复

请参阅[changelog](docs/changelog.txt) 获取所有改进的完整日志。

## 下载

获取最新版本[here](https://github.com/Bioruebe/UniExtract2/releases/download/v2.0.0-rc.3/UniExtractRC3.zip)

###### 病毒警报？

通用提取器不包含任何恶意软件。一些反病毒程序偶尔会误检UniExtract程序目录中的文件。你可以肯定这是一个所谓的假阳性，一个错误-如果你下载UniExtract从官方来源 `https://github.com/Bioruebe/UniExtract2`.更详细的解释可参见 [here](/docs/ANTI-MALWARE.md).如果您遇到误报，请报告 [here](https://github.com/Bioruebe/UniExtract2/issues/78).

###### 'Windows protected your PC'?

Modern versions of Windows have a feature called *SmartScreen*, which warns about unknown files. This means software without a big company behind it and/or a huge userbase produces a warning. Don't panic! Mostly this happens after a new version of UniExtract has been released. After enough users updated their installation, the warning might vanish, because it now has reputation. If you see a *SmartScreen* warning, you can safely click 'More info', then 'Run anyway'.

###### System requirements

In short: Windows XP or newer.
However, outdated version of Windows only have limited support:

- Windows 7: sending feedback requires you to follow [this guide by Microsoft](https://support.microsoft.com/en-us/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-default-secure-protocols-in-wi), otherwise it will fail
- Windows XP: any online functionality, such as the updater or the feedback dialog, is disabled for security reasons. Also some extractors might not work.

(Online functionality for these systems might be restored in a future version of Universal Extractor.)

###### Updating

Universal Extractor 2 comes with a built-in updater. You will receive a notification when a new version is released. Alternatively, you can search for updates manually from the `Help` menu.

At the moment, UniExtract is still in beta and updates are rare. If you want to keep up-to-date with the development, you can [opt-in to more frequent updates](#nightly-builds).

**Do not replace any files in UniExtract's program directory yourself. This will break things!**
More details can be found [here](https://github.com/Bioruebe/UniExtract2/issues/293#issuecomment-1142877436).

###### Older versions

...can be found on the [Releases](https://github.com/Bioruebe/UniExtract2/releases) page.
However, this is for historical reasons ony. Please consider using the newest version instead.

###### Uninstalling

- If you enabled **context menu entries**, open Universal Extractor and select `Edit` > `Context Menu Entries`. Uncheck both `enabled` checkboxes and click `OK`.
- If you saved the program to a directory without write access (e.g. C:\Program Files) and want to remove all settings, remove the directory `%APPDATA%\Bioruebe\UniExtract`. Simply open the file explorer and enter `%APPDATA%\Bioruebe` into the path input, then delete the directory `UniExtract`.
- Finally, delete the program directory.

## FAQ

#### Is there a portable version?

Universal Extractor itself is completely portable, with some exceptions:

- Enabling context menu entries will create registry entries
- To extract a wide variety of file types more than 50 different extractors are used. Some of them might leave traces on the system. For the most common archives and installers extraction can be considered portable, for others probably not.
- Storing Universal Extractor in a directory without write access (e.g. C:\Program Files) enables multi-user mode. This results in configuration files being stored in the %APPDATA% directory (C:\Users\YourUsername\AppData\Roaming\Bioruebe\UniExtract).
  See issue [#20](https://github.com/Bioruebe/UniExtract2/issues/20) for more information.

#### 为什么通用取出器有许多不同的版本/修改/重新包装？

当UniExtract最初的开发者停止开发它时，来自世界各地的许多人继续更新和改进该程序。一些“只”更新了通用提取器使用的工具，其他人添加了伟大的功能。因此，所有版本在支持的归档文件和添加的功能方面有所不同。

这个版本是唯一一个“真实的的”开源版本，在Github上有一个每个人都可以贡献的中央存储库。多年来，我满足了许多用户的要求，增加了对社区想要解压缩的文件的支持，并实现了许多方便的功能。许多志愿者帮助翻译UniExtract、查找bug、讨论改进和回答其他用户的问题。

但是，Universal Extractor 2可能无法解压缩此工具的其他版本可以解压缩的文件。如果您确实需要访问归档文件的内容，您可以使用其他UniExtract之一获得成功。或者，您也可以在这里寻求支持。不过，我可能要等一会儿才能回答。

#### UniExtract可以（重新）压缩文件吗？

否。此工具设计为提取实用程序。对应物（ “统一档案” ）超出范围-至少对我来说是这样。（阅读原因 [here](https://github.com/Bioruebe/UniExtract2/issues/87#issuecomment-409806225).)请随意创建它！

## 夜间构建

您可以选择接收Universal Extractor 2的最新开发版本。只需打开首选项对话框（从“编辑”菜单），并选中安装测试版更新。下次搜索更新时，您将收到开发内部版本，而不是发布版本。再次禁用该选项后，您可以通过简单的更新返回到最新的稳定版本。

## Reporting bugs

Did you encounter a problem with UniExtract? Please report what went wrong to us. There are differnet ways to do so:

- If you have a Github account, you can **[open an issue](https://github.com/Bioruebe/UniExtract2/issues)**. This is the prefered way for **feature requests**, **suggestions** and **general technical problems**.
- From within Universal Extractor: select **'Give feedback'** from the **'Help' menu**. This is the prefered way to submit **failed extractons**. If UniExtract was not successful, it will automatically ask you to send feedback (can be disabled from the options). This type of feedback includes a log with several debug information, which could help fixing the problem.
- Direct contact via **[email](https://bioruebe.com/blog/contact/)**. This can be used if you do not have an account at Github. Many users, who created translations for UniExtract, like to send updated files per email. (Others open [pull requests](https://github.com/Bioruebe/UniExtract2/pulls) instead.)

## Building from Source

1. Download and install [AutoIt](https://www.autoitscript.com/site/autoit/downloads/)
2. Download and install [SciTE](https://www.autoitscript.com/site/autoit-script-editor/downloads/) (Optional)
   - Running UniExtract through SciTE has the additional benefit of real-time logging in the built-in console.
3. Clone this repository **or** download a snapshot and unpack into a folder of your likings
4. Open UniExtract.au3 in SciTE and hit `F5` to run in debug mode; `F7` to build an executable file **or** run UniExtract.au3 through Aut2Exe (look [here](https://github.com/Bioruebe/UniExtract2/issues/72#issuecomment-313288728) for more information about Aut2Exe)
5. Download the necessary program files, which are not part of the source package
   1. Run the program
   2. UniExtract will display a message that the program files are incomplete. Select `No`.
   3. Go to `Edit/Preferences` and check `Install beta updates`. An update notification should appear. Otherwise, choose `Help/Check for Updates`. Select `Yes`.
6. In case the main executable gets overwritten, rebuild it as explained in step 4.

## Contributions

Any contribution in form of ideas, bug reports, code commits, documentation improvements, etc. is welcome. Help is currently needed in updating the translations for many languages. If you are able to translate into another language, take a look at the corresponding issue (#2) or open the language file in the `/lang` subdirectory and check for empty strings. English and German language are always up-to-date and can be used as a reference.

Feel free to submit bug reports or feature requests using the issues tab or the built-in feedback window in Universal Extractor, accessible via the 'Help' menu. Refer to Github's issue page for planned features and problems to be fixed in future versions. The file `todo.txt` is a leftover from the original Universal Extractor and only used for personal development thoughts and notes.

## License

Universal Extractor is licensed under **GPLv2**. See LICENSE for the full legal text.
Code (functions, UDFs, etc.) written from scratch by me (which are not under copyleft) can also be used in your own projects under the terms of a BSD 3-clause license.

Universal Extractor uses [TrIDLib by Marco Pontello](http://mark0.net/code-tridlib-e.html), several [7zip plugins by Dec Software](https://www.tc4shell.com/en/7zip/) and many other great tools and libraries to support as many file formats as possible. Please consider supporting the authors of the software [mentioned here](/docs/helper_binaries_info.txt).

Please note that Universal Extractor includes third-party software, which uses different licenses than the main program. Specifically, **some extractors do not allow commercial use**. If you intend to use the software for commercial purposes, please check the individual license files in the `/docs` subdirectory and the [helper binary info file](https://github.com/Bioruebe/UniExtract2/blob/master/helper_binaries_info.txt) first.
Feel free to delete files, whose license does not fit your use case, from the `/bin` subdirectory.
