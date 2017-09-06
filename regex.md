
http://dotinstall.com/lessons/basic_regexp  

■メタ文字  

大かっこ：任意の一文字：[abc]  
ハイフン：範囲：[a-z]  
キャレット：否定：[^abc]  

ピリオド：任意の一文字  
キャレット：行頭  
ドルマーク：行末  

波かっこ：直前の文字繰り返し数：{}  
0{2} → 00
0{2,} → 00,000,0000,...  
0{2,4} → 00,000,0000  

アスタ：0 or more  
a* → , a, aa, aaa, ...  
はてな：0 or 1 文字繰り返し  
a* → , a  
プラス：1以上の繰り返し  
a* → a, aa, aaa, ...  

カッコ：単位規定：()  
(abc)* → , abc, abcabc, abcabcabc, ...  

縦棒：または：|  
(abc|def) → abc, def  

えんマーク（バックスラッシュ）系  
\n → 改行  
\t → タブ  
\d → 数字[0-9]  
\w → 英数字[a-zA-Z0-9]  
\s → スペース、タブ  
\メタ文字 → エスケープ（メタ文字を普通の文字化）  

アスタやプラス後のはてな：最小マッチ  
xabcyabczabc → .+abc → xabcyabczabc  
xabcyabczabc → .+?abc → xabc  
※grep非対応  
