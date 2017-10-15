# 選挙予測
## モデル評価方法
1. ある選挙を評価データ、その選挙以外を学習データとする。
1. ある選挙の獲得議席上位5政党とその他の合計6カテゴリについて獲得議席を予測する。
1. この作業を学習データのすべての選挙について行い、平均二乗誤差で評価する。
### ノリで書いた数式
- n:選挙の数
- L:実際の獲得議席数。Lkjは、第k回選挙の獲得議席順位j+1位の党の各得票数
- P:予測獲得議席数。Pkjは、第k回選挙の獲得議席順位j+1位の党の各得票数


![metrix](https://raw.githubusercontent.com/rskmoi/election_forecast/master/texclip20171015165144.png "metrix")

## カラム説明
election_id,第何回の選挙か

date_of_dissolution,解散日

date_of_election,投票日

capacity,定員

party,党名

is_government_party,解散時与党フラグ

last_date_of_electon(rep),前回衆議院選挙日

before_seats(rep),衆議院での直前の議席数（前回選挙結果ではない）

last_date_of_electon(cou),前回参議院選挙日

before_seats(cou),前回参議院選挙の結果

candidates,出馬した人の数

approval_rating(last_month),直近の月の支持率

approval_rating(2_month_ago),2ヶ月前の支持率

approval_rating(3_month_ago),3ヶ月前の支持率

result,選挙結果（当選数）

