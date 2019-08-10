# VSCode

> get MONACO font

> get Operator Mono with Ligatures font
```bash
cd ~/Desktop
git clone https://github.com/coderJianXun/Operator-Mono.git
git clone https://github.com/kiliman/operator-mono-lig.git
cd Operator-Mono/src/Operator\ Mono
for x in `ls`; do mv $x `echo $x| sed 's/-/SSm-/'`; done
cd ../../../
mv Operator-Mono/src/Operator\ Mono/* operator-mono-lig/original
cd operator-mono-lig/
npm i
./build.sh
open build
ls | xargs open
```

looks best on Ubuntu & Mac, Windows's user consider using another font

```json
{
	"editor.fontSize": 14,
	// "go.gopath": "~/go",
	"editor.insertSpaces": false,
	"editor.wordWrap": "on",
	"editor.cursorStyle": "line",
	"editor.detectIndentation": true,
	"editor.fontFamily": "OperatorMonoSSmLig-Book",
	"editor.fontLigatures": true,
	"editor.fontWeight": "bold",
	"editor.minimap.renderCharacters": false,
	"editor.mouseWheelZoom": false,
	"editor.smoothScrolling": true,
	"editor.wrappingIndent": "indent",
	"editor.lineHeight": 25,
	"editor.letterSpacing": 1,
	"javascript.format.placeOpenBraceOnNewLineForControlBlocks": true,
	"javascript.format.placeOpenBraceOnNewLineForFunctions": true,
	"typescript.format.placeOpenBraceOnNewLineForFunctions": true,
	"typescript.format.placeOpenBraceOnNewLineForControlBlocks": true,
	"terminal.integrated.fontSize": 14,
	"nasc-touchbar.addCursorBelow": false,
	"nasc-touchbar.gitSync": true,
	"nasc-touchbar.rename": false,
	"nasc-touchbar.showCommands": false,
	"nasc-touchbar.peekDefinition": true,
	"nasc-touchbar.jumpToBracket": true,
	"files.useExperimentalFileWatcher": false,
	"files.autoSave": "afterDelay",
	"files.autoSaveDelay": 10000,
	"editor.cursorBlinking": "expand",
	// "nasc-touchbar.addCursorAbove": true,
	"remotehub.githubToken": "a4945949129c9bb2eee42a0d0988ce045951137b",
	"workbench.colorTheme": "Sam Monokai Dark",
	"C_Cpp.clang_format_style": "file",
	"todohighlight.exclude": [
		"**/node_modules/**",
		"**/bower_components/**",
		"**/dist/**",
		"**/build/**",
		"**/.vscode/**",
		"**/.github/**",
		"**/_output/**",
		"**/*.min.*",
		"**/*.map",
		"**/.next/**",
		"**/platforms/**",
		"**/assets/imgs/Ionic App_files/**",
		"**/plugins/**",
		"**/vendor.js"
	],
	"todohighlight.keywords": [],
	"todo-tree.defaultHighlight": {
		"icon": "verified",
		"type": "text",
		"foreground": "green",
		"background": "transparent",
		"iconColour": "lightgreen"
	},
	"todo-tree.customHighlight": {
		"INFO":{
			"icon": "issue-opened",
			"type": "line",
			"foreground": "blue",
			"background": "green",
			"iconColour": "white"
		},
		"TODO": {
			"icon": "issue-opened",
			"type": "line",
			"foreground": "#ff0000",
			"background": "#FFFFFF",
			"iconColour": "yellow"
		},
		"FIXME": {
			"icon": "alert",
			"type": "line",
			"foreground": "red",
			"background": "white",
			"iconColour": "blue"
		},
		"COMPLETED": {
			"icon": "verified",
			"type": "text",
			"foreground": "#c8ff77",
			"background": "#161616",
			"iconColour": "lightgreen"
		},
		"FUTURETODO":{
			"icon":"watch",
			"type" :"text",
			"foreground":"green",
			"background":"black",
			"iconColour":"white"
		}
	},
	"todo-tree.tags": [
		"INFO",
		"TODO",
		"FIXME",
		"COMPLETED",
		"FUTURETODO"
	],
	"files.associations": {
		"*.cpp": "cpp"
	},
	"workbench.startupEditor": "newUntitledFile",
	"java.errors.incompleteClasspath.severity": "ignore",
	"breadcrumbs.enabled": true,
	"window.zoomLevel": -1,
	"window.closeWhenEmpty": true,
	"window.nativeTabs": true,
	"window.restoreWindows": "all",
	"workbench.editor.enablePreview": false,
	"workbench.editor.swipeToNavigate": true,
	"workbench.editor.tabCloseButton": "off",
	"workbench.editor.tabSizing": "shrink",
	"window.newWindowDimensions": "fullscreen",
	"window.openFilesInNewWindow": "on",
	"explorer.openEditors.visible": 0,
	"search.smartCase": true,
	"editor.minimap.showSlider": "always",


	// FROM KL
	"code-runner.executorMap": {
        "cpp": "g++ main.cpp -o main.o && ./main.o < in.txt"
    },
    "files.associations": {
        "stack": "cpp",
        "ostream": "cpp",
        "istream": "cpp"
	},
	"todo-tree.statusBar": "top three",
}
```
