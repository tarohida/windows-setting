# windows-setting

windowsの設定をメモするレポジトリ

## Download, Documents等のパーティションを, Dドライブ以下フォルダに移動する.

対象フォルダ

- Desktop
- Documents
- Downloads
- Music
- Pictures
- Videos

## 3D Objects, Favorites等ファイルについて、CLIから表示されないよう, プロパティを "hidden" に設定する.

フォルダの右クリック > プロパティ > Hidden にチェックを入れてApply.  
選択肢は、"Apply changes to this foloder only" でよい.  

<p>適用前</p>

```
PS C:\Users\taro_hida> dir


    Directory: C:\Users\taro_hida


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-r---        10/3/2020  10:54 AM                Desktop
d-r---        10/6/2020   9:25 AM                Documents
d-r---        10/2/2020   5:58 PM                Downloads
d-r---        9/10/2020   7:55 AM                Links
d-r---        9/10/2020   7:55 AM                Music
dar--l        10/6/2020   8:02 AM                OneDrive
d-r---        9/23/2020   5:57 PM                Pictures
d-r---        9/10/2020   7:55 AM                Videos
```

<p>適用後</p>

```
PS C:\Users\taro_hida> dir


    Directory: C:\Users\taro_hida


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-r---        10/3/2020  10:54 AM                Desktop
d-r---        10/6/2020   9:25 AM                Documents
d-r---        10/2/2020   5:58 PM                Downloads
d-r---        9/10/2020   7:55 AM                Music
dar--l        10/6/2020   8:02 AM                OneDrive
d-r---        9/23/2020   5:57 PM                Pictures
d-r---        9/10/2020   7:55 AM                Videos
```

## C:\Users\user_name\projects フォルダの作成

プロジェクトを格納するディレクトリを作成する．Homesteadなど仮想環境から参照されたり，IDEから参照されたりする．  
ここに設置しておけば，CLIから遷移しやすくなるので非常に便利．
