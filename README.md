## electron sample application

Electronのtutorialを触る。

WSL2だと何やらうまく動かない部分が多く、試行錯誤必要。

参考:
- [WSL2でElectron開発する方法(VcXsrvなし)](https://zenn.dev/test_myname/articles/e5bb778d320e79)
- [Vue3+ElectronでのWindowsアプリ開発](https://zenn.dev/atoz/articles/8e44a377fe589f)
- ["GPU process isn't usable. Goodbye."](https://stackoverflow.com/questions/68874940/gpu-process-isnt-usable-goodbye) WSL2でelectronを動かそうとすると、`[4908:0306/014851.990:ERROR:gpu_process_host.cc(947)] GPU process launch failed: error_code=18`, `[4908:0306/014851.990:FATAL:gpu_data_manager_impl_private.cc(440)] GPU process isn't usable. Goodbye.`といったエラーが出て、動かない。その対処法。（index.jsに`app.commandLine.appendSwitch('in-process-gpu');`の記述を追加）