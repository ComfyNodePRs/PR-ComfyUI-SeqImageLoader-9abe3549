# ComfyUI Sequential Image Loader

## Overview
これはGUI上でフレーム毎にマスキング(とスケッチ)を行うためのComfyUI用の拡張ノードです。  

## Usage

### ノードについて
#### input
* sequence_id: 無視してください (内部処理でのみ使います)。  
* upload button: ダイアログから動画のフレームを含むディレクトリ世指定します。  
* start_index: 開始フレーム番号を指定します。0で無効。  
* end_index: 終了フレーム番号を指定します。0で無効。  
#### output
* images: 読み込んだフレームデータです。スケッチした場合、その内容が適用されます。  
* mask_images: 各フレームのマスクが画像として出力されます。Mask To Imageノード等でマスクデータに変換が必要です。  
* image_count: 処理フレーム数。  

### マスクエディターについて
	1. フレームを読み込んだ後にノードを右クリックして、"Open In MaskEditor"を選択します。  
	2. 出現したエディタ上でマスキングと必要に応じてスケッチを行います。  
	
## Example


## Other
input/ディレクトリに作業中の一時フレームデータが溜まっていくので、適当なタイミングで使わなくなったデータを削除してください。  