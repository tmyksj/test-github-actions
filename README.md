# test-github-actions
github actions を試した記録。

# やったこと
1. Initial commit  
9110121bf73ef356d1cae300638987f7c8920250  
1. Simple workflow を追加してみる。  
追加後に actions が動作したことを確認。  
8b6b0c856b05ac95b9628efa778edfc7a82e449d  
1. Node.js を使って、 jobs.<job_id>.strategy の挙動を確認。  
各条件それぞれで動作したことを確認。  
9ab0ae8f1791c0d3ce72cc77ae0dbcd74bad48cc  
1. プルリクエストの検証のため、もとに戻して、 script.sh を追加。  
974ce34105b7c590298ea90f71394027bcd37c9c  
60ed7a5910b8409ce6fc872f64de167e866bd4b9  
1. ブランチを分けて、 actions に script.sh を実行するコマンドを追加し、プルリクエストを作成。  
script.sh は +x でないので、実行できずに落ちる。  
プルリクエストは、マージできる状態だったので、 Settings から master を保護して、マージできないように設定。  
4814bda8d11b9e4e8da699d0c1de4f82af3c8cdd  
1. script.sh は sh を介すると +x でなくても実行できるので、それに変更。  
actions も通る。  
マージもできるようになったので、 master にマージ。  
マージ後は、 actions が master で動作したことを確認。  
45e86d29a52125e875abb318af0223646804f749  
1db23c115f994becab77fd25b69d8df0da5d780f  
