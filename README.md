 1. Отобразить подключённый девайс в консоли.

adb devices

 2. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB

adb install todo.apk

 3. Вывести адрес приложения todolist в системе Android

adb shell pm list packages -f | findstr todolist

 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.

adb exec-out screencap -p > 1_todolist.png

 5. Вывести в консоль логи приложения todolist

adb logcat | findstr com.android.todolist

 6. Скопировать логи приложения todolist на компьютер.

adb logcat | findstr com.android.todolist > todo.log

 7. Удалить приложение todolist с телефона через ADB

adb uninstall com.android.todolist
