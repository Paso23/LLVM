## Metodi di utilizzo
Dopo aver scaricato i file di configurazione eseguire i seguenti comandi:

- LocalOpts.h -> <code>SRC_ROOT/llvm/include/llvm/Transforms/Utils</code>
- LocalOpts.cpp -> <code>SRC_ROOT/llvm/lib/Transforms/Utils/</code>
  <br>
  In seguito si può ricompilare opt nella cartella BUILD col seguente comando <code>make opt</code>
  <br>
  Dopo aver ricompilato è possibile andare nella root directory di LLVM(quella in cui sono presenti le directory BUILD,TEST,SRC,INSTALL) ed eseguire i seguenti comandi:

```
  export PATH=/root/LLVM_ROOT/install/bin:$PATH\
  build/bin/opt -p localopts test/ass1.ll -o test/ass1.optimized.bc
  cd test
  llvm-dis ass1.optimized.bc -o ass1.opt.ll
```
