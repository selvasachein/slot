# Ex02 Time Table
## Date:

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create an App inside the Django project.

### STEP 2
Create a static folder uder the created App and insert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html with the relevant attributes.

### STEP 4
Add rows using ```<tr>``` tag.

### STEP 5
Add your course schedule using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM


## OUTPUT


## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.

## クラッシュ復旧方針（SwiftData）

### 目的
ローカル永続データの不整合や破損が起きた場合でも、起動時クラッシュを回避し、ユーザー同意のうえで復旧できる導線を提供する。

### 対象範囲
1. `ModelContainer` 生成失敗時に起動直後の `fatalError` / `assertionFailure` を使わず、復旧可能なエラーハンドリングに置き換える。
2. 復旧可能な場合はブロッキングダイアログを表示する。
   - 文言: `登録データが不整合です。データをクリアしますか？`
   - 操作: `はい` / `キャンセル`
3. ユーザーが `はい` を選択した場合はローカルストアを削除し、`ModelContainer` を再初期化する。
4. `キャンセル` の場合は中途半端に起動せず、明示的なエラー画面で安全に停止する。

### 実装アプローチ
1. 永続コンテナの起動処理を専用の起動コーディネーターに切り出す。
2. 初期化状態を SwiftUI ルートに公開する（`loading` / `ready` / `recoveryRequired` / `failed`）。
3. ストア削除処理はアプリ管理下の永続ファイルのみに限定する。
4. 削除後にコンテナを再初期化し、通常起動へ復帰させる。

### 運用上の注意
1. 本復旧ではローカルデータが消去されるため、ユーザー同意を必須とする。
2. TestFlight で追跡可能にするため、初回失敗理由と復旧結果を構造化ログで記録する。
3. 長期的にはマイグレーション対応を優先し、リセット導線は非復旧時のフォールバックとして扱う。
