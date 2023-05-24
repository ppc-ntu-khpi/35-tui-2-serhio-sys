[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-7f7980b617ed060a017424585567c406b6ee15c891e84e1186181d67ecf80aa0.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=11217830)
# UI Lab 2 

## На "чотири"
1. Перепишіть код  так, щоб інформація про клієнтів банку та їх рахунки читалась з файлу **test.dat** (робота номер 8, [файл даних](https://github.com/liketaurus/TUI-Labs/blob/master/data/test.dat) також є в цьому ж репозиторію).
2. Запустіть проект, впевніться, що все працює як очікувалось. Продемонстрируйте результат викладачеві.
![](/images/1.png)
![](/images/2.png)
``` java
public static void main(String[] args) throws IOException {
        File currentClass = new File(URLDecoder.decode(CLIdemo.class
                .getProtectionDomain()
                .getCodeSource()
                .getLocation()
                .getPath(), "UTF-8"));
        String classDirectory = currentClass.getParent();
        //Loading saved data
        dataSource = new DataSource(classDirectory+"\\35-tui-2-serhio-sys\\test.dat");
        dataSource.loadData();
        //Loading saved data
        CLIdemo shell = new CLIdemo();
        shell.init();
        shell.run();
    }
```
## На "п'ять"
1. Додайте ще одну команду - **report**, яка має виводити звіт за клієнтами такого ж виду, як у роботі номер 8 (див. CustomerReport).
2. Запустіть проект, впевніться, що все працює як очікувалось. Продемонстрируйте результат викладачеві.
![](/images/6.png)

# Додаткові завдання
Для тих, хто бажає отримати ще одну (або кілька) гарну оцінку - спробуйте наступне:
- Додайте команду **account** - можливість **працювати з рахунками** клієнта (обирати рахунок для перегляду балансу)
- Додайте команди **deposit**, **withdraw** для **зарахування або зняття коштів** з обраного рахунку обраного клієнта
- Додайте команду **save** для **зберігання оновленої інформації** про клієнтів банку та їх рахунки до файлу **test.dat**
![](/images/3.png)
![](/images/4.png)
![](/images/5.png)
