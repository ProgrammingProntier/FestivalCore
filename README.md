# FestivalCore

## 概要

同志社大学のUnreal Engine専門のゲーム開発団体Programming.Prontier();が制作した、ローカルマルチプレイヤーの対戦ゲーム集です。  
本プロジェクトファイルには、外部のアセットを除いて修正を加えたコア部分と一部のゲームのみが含まれています。

開発環境はUnreal Engine 5.0.3です。  
正しく動作させるには[UI Navigation](https://www.unrealengine.com/marketplace/ja/product/uinavigation)プラグイン（無料）が必要です。

## 関連リンク

* [実行ファイル - Google ドライブ](https://drive.google.com/file/d/1kl4Eykp3jpHxiFuciUquo4LCrxfS7uh0/view?usp=sharing)
* [【UE5】大学生チームのローカルマルチプレイヤーゲーム開発事例 - Qiita](https://qiita.com/suramaru517/items/91194a937981b5685341)

## 新規ゲームの作り方

1. コンテンツ作成のメニューからFestivalGameを選択し、`YourName`に自分の名前、`GameName`にゲームの名前を入力して、OKを選択する。  
   `Content/[自分の名前]/[ゲームの名前]`以下にGameMode、PlayerController、DataAssetの3つが作成されたことを確認する。

2. 任意のレベルを作成し、ワールドセッティングの`ゲームモードオーバーライド`に1で作成したGameModeを設定する。  
   レベルを新規作成する場合は、ファイル > 新規レベル > Basicから作成するのがおすすめ。

3. 1で作成したDataAssetを開き、`Level`に2で作成したレベルを設定する。  
   その他のプロパティは任意で設定する。

4. 1で作成したPlayerControllerを開き、`MappingContexts`にゲーム開始時に追加するMappingContextを設定する。  
   TemplatesプラグインのコンテンツにFirstPersonやThirdPersonのMappingContextを用意しているので、それを設定するのがおすすめ。

5. 任意のPawnを作成する。  
   Templatesプラグインのコンテンツにローカルマルチプレイヤー用にセットアップしたFirstPersonCharacterやThirdPersonCharacterを用意しているので、それを継承して作成するのがおすすめ。

6. 1で作成したGameModeを開き、`GameData`に3で設定したDataAsset、`PlayerControllerClass`に4で設定したPlayerController、`DefaultPawnClass`に5で作成したPawnを設定する。

7. `Content/Core/Data/DA_GameSelect`の`AllGameData`に1で作成したDataAssetを追加すると、ゲームセレクトにゲームが表示されるようになる。

## Credits

* [Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts/) - by Nicolae Berbece under CC0
* [M PLUS 1p](https://fonts.google.com/specimen/M+PLUS+1p?subset=japanese&noto.script=Jpan) - by Google Fonts under Open Font License

## License

Those listed in the credits remain under that license.  
Others developed by Programming.Prontier(); are under CC0.
