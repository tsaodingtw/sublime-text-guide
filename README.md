# Sublime Text 入坑指南

Sublime Text 是一套十分受歡迎的文字編輯器，
因爲有豐富的快速鍵功能，強大的套件庫，以及高度的可自訂性，它很適合作爲個人化的開發環境。
本文將爲大家介紹這個優秀的編輯器，並引導讀者在數分鐘之內將 Sublime Text 配置成爲個人化的 IDE。

## 安裝主程式

Sublime Text 是商業軟體，你可以在官方網站免費下載試用版，而試用期是**無限**的。
除了偶爾會在存檔時詢問你是否要購買，試用版與正式授權版並無任何分別。
目前一份授權的售價是 70 美元，可以到[這裏](http://www.sublimetext.com/buy)購買。

#### Windows/Mac OS X

到這裏下載：
http://www.sublimetext.com/3

#### Linux (Ubuntu/Mint)

建議用系統的套件管理來安裝，在 terminal 輸入：

``` shell
$ sudo apt-get install sublime-text
```

## 基本操作

* 與其它編輯器相似，<kbd>Ctrl</kbd> + <kbd>O</kbd> 開啓檔案，<kbd>Ctrl</kbd> + <kbd>S</kbd> 存檔，另存新檔則是 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd>。
* 類似 Chromium 瀏覽器的操作，<kbd>Ctrl</kbd> + <kbd>N</kbd> 開新檔案（開新分頁），<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>N</kbd> 開新視窗，<kbd>Ctrl</kbd> + <kbd>W</kbd> 關閉分頁，<kbd>Ctrl</kbd> + <kbd>Tab</kbd> 切換分頁，<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Tab</kbd> 切換到上個分頁。拖曳分頁可以重新排序，將分頁拖出視窗可以開新視窗。
* <kbd>Shift</kbd> + <kbd>↑</kbd>/<kbd>↓</kbd>/<kbd>←</kbd>/<kbd>→</kbd> = 選取，<kbd>Ctrl</kbd> + <kbd>←</kbd>/<kbd>→</kbd> = 一次移動一個字
* <kbd>Ctrl</kbd> + 點擊 = 多重編輯
* <kbd>Ctrl</kbd> + <kbd>D</kbd>：選取這個字，按第二下以上的話會向下尋找並選取所有相符的字（多重編輯）。
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>↑</kbd>/<kbd>↓</kbd>：將這行往上/下移動。
* <kbd>Ctrl</kbd> + <kbd>M</kbd>：移動到這一層的下/上括號，再加上 <kbd>Shift</kbd> 就可以容易地將括號內全選。
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>K</kbd>：刪除一整行
* Sublime Text 會自動暫存所有未儲存的資料，就算在未存檔的情況下離開 Sublime Text，甚至關機，資料都不會遺失。

上述的快速鍵功能其實都可以在選單中找到，有空不妨翻翻選單，看看有哪些功能，選單上也會附註該功能的快速鍵。<br/>
更多快速鍵可以到以下網頁查詢：
* [Windows/Linux](http://docs.sublimetext.info/en/latest/reference/keyboard_shortcuts_win.html)
* [Mac OS X](http://docs.sublimetext.info/en/latest/reference/keyboard_shortcuts_osx.html)

## 安裝套件

Sublime Text 有龐大的套件庫可供選擇，在安裝套件之前，建議先將 Package Control 裝起來。
之後你可以到[這裏](https://packagecontrol.io/browse)瀏覽可用的套件，不妨找找有無適合自己的擴充套件。

### 安裝 Package Control

Package Control 是 Sublime Text 的套件管理系統，所有的套件都可以用它來安裝、更新與移除。

依照官網的指示來安裝：https://packagecontrol.io/installation

翻譯如下：

> 複製下面的 Python code，然後在 Sublime Text 中按下 <kbd>Ctrl</kbd> + <kbd>\`</kbd> 打開 console（或者 `View > Show Console`）,貼上剛剛複製的 code，再按 <kbd>Enter</kbd>，就會執行安裝了。

安裝完成之後，請先重啓 Sublime Text。
用 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> 叫出指令面板（或者 `Preference > Package Control`），
輸入「install package」即可瀏覽可用的套件，輸入欲安裝的套件名稱即可安裝。

### 套件推介

#### All Autocomplete

內建的補完功能並沒有支援 STL 中一些常用的東西，好在 Sublime Text 會自動學習目前檔案中寫過的關鍵字。安裝了這個套件之後，不止編輯中的檔案，所有開啓中的檔案內用過的關鍵字都會被學習起來。

#### Alternate VIM Navigation

使用 <kbd>Alt</kbd> + <kbd>I</kbd>/<kbd>J</kbd>/<kbd>K</kbd>/<kbd>L</kbd> 來上下左右移動游標，
<kbd>Alt</kbd> + <kbd>H</kbd>/<kbd>;</kbd> 以將游標移動至行首/行尾，
在自動完成選單中也可以用這個方式在候選詞中上下移動，令右手不必再離開打字區。
亦可以搭配 <kbd>Shift</kbd> 選取文字、<kbd>Ctrl</kbd> 逐字移動等等。
筆者對這個套件的依賴已經到了沒裝它就不知如何移動游標的程度了。

#### C++ Starting Kit

這個套件提供更多 C++ 的自動完成模板，也提升了對 C++ syntax highlighting 的相容性（簡單地說，語法上色變漂亮了）。更多說明請見[這裏](https://packagecontrol.io/packages/C%2B%2B%20Starting%20Kit)。

#### AceJump

![AceJump](https://cloud.githubusercontent.com/assets/8056203/10858871/92069504-7f58-11e5-8593-e373121fd917.gif)

這個功能來自另一款受歡迎的編輯器 Emacs。

使用以下快速鍵瞬移到畫面中的任何位置：
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>;</kbd> 移動到目標字
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>'</kbd> 移動到目標字元 
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>.</kbd> 移動到目標行

更多說明請見[這裏](https://packagecontrol.io/packages/AceJump)。

#### AdvancedNewFile

![AdvancedNewFile](https://cloud.githubusercontent.com/assets/9604053/11331052/4bb42544-91f0-11e5-9296-0edd78e503ca.png)

一個介面漂亮的檔案瀏覽器，將資料夾拖進側邊欄即可放入檔案櫃，更多說明請見[這裏](https://packagecontrol.io/packages/AdvancedNewFile)。

#### Vintageous

完全模擬偉大的 Vim 編輯器的操作方式，無論你是從 Vim 轉換到 Sublime Text，或想要學會用 Vim，都很適合安裝這個套件。

## 將 Sublime Text 打造成爲 IDE

Sublime Text 本身只有文字編輯器，若要編譯程式碼，我們需要另行安裝編譯器。
Sublime Text 中提供了 Build System 這個功能，方便使用者自行整合想用的編譯器。
這部分將說明如何安裝 GCC 作爲 C++ 的編譯器，並示範用 Build System 來設定「編譯並執行」的功能。

### 安裝 GCC

#### Windows

這裏推薦 Windows users 使用 TDM-GCC 而非 MinGW，因爲前者的安裝較爲簡單，不需經過繁複的設定。
（另外筆者也曾被 MinGW 的 bug 雷過……）

到這裏下載：http://tdm-gcc.tdragon.net/download

#### Linux

一樣建議用系統的套件管理安裝，建議將 g++ 一併裝起來。

``` shell
$ sudo apt-get install g++
```

#### Mac OS X

要在 OS X 底下裝 GCC，最簡單的方法就是安裝 Xcode，如果你的 Mac 裏面有 Xcode，就已經有 GCC 了。
若要安裝 Xcode，在 Terminal 下輸入：

``` shell
$ xcode-select --install
```

### 使用 Build System 建立編譯腳本

Build System 是編譯指令的腳本，透過它我們可以一鍵完成編譯指令。

工具列中的 `Tools > Build System` 裏面已經內建了一些常用語言的 Build System。但內建的 Build System 不是很好用，如果想要「編譯並執行」的功能，或加入自己想要的編譯參數，我們可以選擇 `Tools > Build System > New Build System` 來建立自訂的 Build System。

Build System 是 JSON 格式，如果不會寫也不緊要，因爲 ~~筆者也不會~~ 下面的範本可以直接拿來用。

這裏給出筆者自己使用的 Build System，其效果相當於執行以下的編譯指令，接着執行編譯完成的程式：

``` shell
$ g++ -Wall -lm -lcrypt -O2 -std=c++11 -pipe -[檔案名稱]
```

#### Windows

``` json
{
    "variants":
    [
        {
            "name": "Run",
            "shell_cmd": "g++ $file -Wall -lm -O2 -std=c++11 -pipe && start cmd /k a"
        }
    ]
}
```

#### Linux

``` json
{
    "variants":
    [
        {
            "name": "Run",
			"shell_cmd": "g++ $file -Wall -lm -lcrypt -O2 -std=c++11 -pipe && gnome-terminal -x bash -c \"./a.out; read -p \\\"[Press any key]\\\"\""
        }
    ]
}
```

#### Mac OS X

``` json
{
    "variants":
    [
        {
            "name": "Run",
            "shell_cmd": "g++ $file -Wall -lm -O2 -std=c++11 -pipe && open -a Terminal ./a.out"
        }
    ]
}

```
