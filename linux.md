- ps aux | grep zhiyitodb | awk '{print $1}' | xargs kill -9
> - 批量杀死带zhiyitodb的进程
