## Metodi di utilizzo
Dopo aver scaricato i file di configurazione eseguire i seguenti comandi:

Copiare i seguenti file nelle rispettive directory:
- guardFuse.ll e unguardFuse.ll -> <code>test/</code>
- LoopFusionPass.h -> <code>SRC_ROOT/llvm/include/llvm/Transforms/Utils</code>
- LoopFusionPass.cpp -> <code>SRC_ROOT/llvm/lib/Transforms/Utils/</code>\
  <br>
  In seguito si può ricompilare opt nella cartella build col seguente comando <code>make opt</code>\
  <br>
  Dopo aver ricompilato è possibile andare nella root directory di LLVM(quella in cui sono presenti le directory BUILD,TEST,SRC,INSTALL) ed eseguire i seguenti comandi:\

```
  export PATH=/root/LLVM_ROOT/install/bin:$PATH\
  build/bin/opt -p loopfusionpass test/LOOP.ll -o test/FINAL.bc\
  cd test
  llvm-dis FINAL.bc -o FINAL.ll
```
