# c-interpreter-practice
the code is from:https://github.com/lotabout/write-a-C-interpreter

實作心得：
依照教學實作一個c語言的直譯器，以下是我對程式碼的理解

分配symbol table, text, data, stack的記憶體空間。把token保留字載入symbol table(e.g. while, return, etc) 再把虛擬機指令載入symbol table。讀取source code，program()會以token為單位讀取並使用類似BNF遞迴把statement拆成expression，遞迴至能用虛擬機指令處理把指令放到text區塊全域變數放到data區塊。最後執行虛擬機，模擬程式runtime的stack操作。
