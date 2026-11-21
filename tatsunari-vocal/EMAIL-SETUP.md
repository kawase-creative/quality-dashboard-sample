# 予約メールの設定

送信先: tatsunari.vocal.lesson@gmail.com
送信バックエンド: FormSubmit AJAX API（https://formsubmit.co/ajax/tatsunari.vocal.lesson@gmail.com）
公式手順: https://formsubmit.co/ と https://formsubmit.co/ajax-documentation

## 有効化が必要

1. 公開ページでテスト用の内容を入力し、確認画面の「予約希望を送信する」を押す。
2. tatsunari.vocal.lesson@gmail.com に届く FormSubmit の確認メールを開き、有効化する。迷惑メールも確認する。
3. 公開ページから再度テストし、第1〜第3希望を含む予約メールが届くことを確認する。

送信先を tatsunari.vocal.lesson@gmail.com に変更。新しい送信先へのテスト送信・有効化・到着確認は未実施。公開ページは有効化要求・送信失敗を成功扱いしない。FormSubmitの正常応答時も「送信サービスが受け付けました」と表示し、到着や予約確定を断言しない。

## 動作

メールアプリは起動せず、サイトからFormSubmitへ入力情報をPOSTする。第1希望は必須、第2・第3希望は任意。送信中はボタンを無効化し、失敗・タイムアウト時には入力を保持する。再送で重複する場合があるため注意文を表示する。返信先は申込者のメールアドレス。個人情報をブラウザ内の予約管理デモに保存しない。admin.html は過去のローカルデータ用デモで、本番予約管理ではない。

FormSubmitを利用することをフォーム上で明示。送信内容は同サービスを経由する。APIキーやGmailパスワードは不要。サービスの制限や迷惑メール判定等により届かない場合はLINEへ案内する。運用開始前に上記の有効化と受信確認を完了する。
