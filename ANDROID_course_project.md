## Basic Android social application

**Goal**   
Learn how to develop Android applications. Get practical skills.<br>
Application development includes different topics of Android application development, like:<br>
Android OS \- understand Android OS architecture and core components.<br>
Activity \- understand Activity lifecycle and usage in Android application development.<br>
Fragment \- understand how to design application with fragments. Understand fragments lifecycle. How to organize communication between Activity and Fragment.<br>
Views \- understand how to design UI elements by using different View components.<br>
RecyclerView \- understand how to use fill complex arrays/lists of data into ListView, GridView and other components.<br>
REST API \- understand how to get/ create/ update/ remove data on remote server. How to communicate with remote servers.<br>
Retrofit/ Glide \- understand how to use popular image loading libraries.<br>
Android MVP \- understand key components of MVP Android application design.<br>

**Project description**  
Application has several screens with different functionality. There are 2 main groups of application components:<br>

### Authorization group:<br>

- Login screen<br>
- Sign up screen<br>
- Forgot password<br>

### Main screen group:<br>

- Profile screen<br> 
- Posts screen<br>
- Comments screen<br> 
- Albums screen<br>
- Images screen<br>
- Todos screen<br>

Application can communicate with remove server and get different data about:<br>

- Users<br>
- Posts<br>
- Comments<br> 
- Albums<br>
- Images<br>
- Todos<br>

Open Test REST API documentation: 
[https://github.com/typicode/jsonplaceholder](https://github.com/typicode/jsonplaceholder) <br><br>  
**Recommended steps to build such application:**

1. **Activity lesson**  
   1. **Create demo project with Authorization activity.**

   At this stage, install Android Studio and create a new project.<br>
      Choose the package name as follows:<br>

   com.pllug.course.your surname in English, in lowercase.<br>

   Set the Activity name \-\> **AuthorizationActivity**.

   Set the Layout name \-\> **activity\_authorization**.

2. **View lesson**  
   1. **Create initial design for login screen.**

   Create a basic design for the user login screen.<br>
      The login screen must contain username and password fields. Also add a button to confirm login.<br>

3. **Intent lesson**  
   1. **Create initial design for Profile screen**  
      Create an additional Activity \-\> MainActivity.<br>
      Create a new layout file \-\> activity\_main.<br>
      Create a basic user profile design. The user profile consists of:<br>
      a profile image (use a fixed image),<br>
      the username,<br>
      a user description.<br>
   2. **Implement user input validation logic (email, password are not empty).**  
      In AuthorizationActivity, implement basic validation for the username and password fields (check that the fields are not empty).<br>
   3. **Implement logic to move from Authorization activity to MainActivity.**
   	If the user clicks Login and the username and password are valid, navigate from AuthorizationActivity \-\> MainActivity.<br>

4. **Fragment lesson**  
   1. **Implement basic logic for SignInFragment**  
      Move the design and validation logic from AuthorizationActivity into a new SignInFragment. The fragment must contain Sign Up and Forgot password buttons.<br> 
      	When Sign In is clicked, navigate to MainActivity. Also implement navigation between the screens when the corresponding buttons are clicked.<br>
   2. **Create initial design for sign up screen.**
   A user may not yet have an account, so create a registration fragment (SignUpFragment). The fragment must contain fields for a username, email address, and initial password. It must also contain buttons to confirm registration (Sign Up), open the login screen (Sign In), and recover a password (Forgot password).<br> 
      	In SignUpFragment, implement basic input validation. When Sign Up is clicked, navigate to MainActivity. Also implement navigation between the screens when the corresponding buttons are clicked.<br>

   3. **Create initial design for forgot password screen.**
   Create a password recovery fragment (ForgotPasswordFragment). The fragment must contain an email address field and a confirmation button (Send new password).<br>
      	In ForgotPasswordFragment, implement basic input validation. When Send new password is clicked, navigate to LoginFragment.<br>

5. **Databases lesson**  
   1. **Learn how to use Adapters and RecyclerView**  
      Study examples of using adapters. They will be used later to display lists of posts, comments, albums, and images.<br>
   2. **Implement basic ProfileFragment**  
      Move the design and validation logic from MainActivity into a new ProfileFragment.<br>
   3. **Implement basic NavigationDrawer**

   Example: [https://developer.android.com/training/implementing-navigation/nav-drawer.html](https://developer.android.com/training/implementing-navigation/nav-drawer.html) <br>

   Create a basic navigation drawer. It will let users navigate between screens (profile, posts, albums, etc.). <br>

6. **Networking lesson**  
   1. **Create data models for Album and Image.**

   Create model classes to represent album and image data. Manually create classes with the same fields as in the examples:<br>

   Albums [http://jsonplaceholder.typicode.com/albums/1](http://jsonplaceholder.typicode.com/albums/1)<br>

   Photos [http://jsonplaceholder.typicode.com/photos/1](http://jsonplaceholder.typicode.com/photos/1)<br>

   2. **implement basic api calls to get list of albums.**

   Use **Retrofit** to request the list of albums. Implement **AlbumRepository** with methods to load all albums and a specific album.<br>

   3. **implement basic api calls to get list of images.**

   Use **Retrofit** to request the list of images. Implement **ImageRepository** with methods to load all images in an album.<br>

   4. **Learn how to use Picasso or Glide image loading library.**
   Explore how to integrate and use image loading libraries.<br>

   5. **Implement basic AlbumsFragment**
   Implement a fragment containing a list that displays album information.<br>

   6. **Implement basic ImagesFragment**
   Implement a fragment containing a list that displays a grid of loaded images.<br>

7. **Files, Shared preferences lesson**  
   1. **Create data models for Profile, Post and Comment.**
   Create model classes to represent profile, post, and comment data. Manually create classes with the same fields as in the examples:<br>

   Profile [http://jsonplaceholder.typicode.com/users/1](http://jsonplaceholder.typicode.com/users/1)<br>

   Post [http://jsonplaceholder.typicode.com/posts/1](http://jsonplaceholder.typicode.com/posts/1)<br>

   Comment [http://jsonplaceholder.typicode.com/comments/1](http://jsonplaceholder.typicode.com/comments/1)<br>

   2. **implement basic api calls to get list of profiles.**

   Use **Retrofit** to request the list of users. Implement **ProfileRepository** with methods to load all profiles and an individual profile by its ID.<br>

   3. **implement basic api calls to get list of posts.**

   Use **Retrofit** to request the list of posts. Implement **PostRepository** with methods to load all posts and an individual post by its ID.<br>

   4. **implement basic api calls to get list of comments.**

   Use **Retrofit** to request the list of comments. Implement **CommentRepository** with methods to load all posts and an individual post by its ID.<br>

8. **Service AsyncTask lesson**  
   1. **Implement basic PostsFragment**

   Implement a fragment containing a list that displays post information.<br>

   2. **Implement basic CommentsFragment**

   Implement a fragment containing a list of comments for a given post.<br>

9. **Sensors lesson**  
   1. **Create data model for Todo.**

   Create a model class to represent todo data. Manually create a class with the same fields as in the example:<br> 
   Todo [http://jsonplaceholder.typicode.com/todos/1](http://jsonplaceholder.typicode.com/todos/1)<br>

   2. **implement basic api calls to get list of todos.**

   Use **Retrofit** to request the list of todos. Implement **TodoRepository** with methods to load all todos.<br>

   3. **Implement basic TodoFragment**

   Implement a fragment containing a list of todos.<br>

10. **Final lesson**  
    1. **Finalize your application.**
    Finish the application and fix any bugs.<br>

---

## Базовий соціальний застосунок для Android

**Мета**   
Навчитися розробляти застосунки для Android. Здобути практичні навички.<br>
Розробка застосунку охоплює різні теми розробки для Android, зокрема:<br>
Android OS \- зрозуміти архітектуру ОС Android та її основні компоненти.<br>
Activity \- зрозуміти життєвий цикл Activity та його використання під час розробки застосунків для Android.<br>
Fragment \- зрозуміти, як проєктувати застосунок із фрагментами, їхній життєвий цикл та організацію взаємодії між Activity і Fragment.<br>
Views \- зрозуміти, як створювати елементи інтерфейсу за допомогою різних компонентів View.<br>
RecyclerView \- зрозуміти, як відображати складні масиви та списки даних у ListView, GridView та інших компонентах.<br>
REST API \- зрозуміти, як отримувати, створювати, оновлювати та видаляти дані на віддаленому сервері й взаємодіяти з віддаленими серверами.<br>
Retrofit/ Glide \- зрозуміти, як використовувати популярні бібліотеки для завантаження зображень.<br>
Android MVP \- зрозуміти основні компоненти проєктування Android-застосунків за підходом MVP.<br>

**Опис проєкту**  
Застосунок має декілька екранів із різними функціями. Компоненти застосунку поділяються на дві основні групи:<br>

### Група авторизації:<br>

- Екран входу<br>
- Екран реєстрації<br>
- Відновлення пароля<br>

### Група основних екранів:<br>

- Екран профілю<br> 
- Екран дописів<br>
- Екран коментарів<br> 
- Екран альбомів<br>
- Екран зображень<br>
- Екран завдань<br>

Застосунок може взаємодіяти з віддаленим сервером та отримувати різні дані про:<br>

- Користувачів<br>
- Дописи<br>
- Коментарі<br> 
- Альбоми<br>
- Зображення<br>
- Завдання<br>

Відкрита документація тестового REST API: 
[https://github.com/typicode/jsonplaceholder](https://github.com/typicode/jsonplaceholder) <br><br>  
**Рекомендовані кроки для створення такого застосунку:**

1. **Заняття з Activity**  
   1. **Створити демонстраційний проєкт з Activity для авторизації.**

   На даному етапі необхідно встановити AndroidStudio та створити новий проект.<br>
      Ім”я пакету варто вибрати наступним чином:<br>

   сom.pllug.course.ваше прізвище англійською мовою і маленькими символами.<br>

   Вказати назву Activity \-\> **AuthorizationActivity**.

   Вказати назву Layout \-\> **activity\_authorization**.

2. **Заняття з View**  
   1. **Створити початковий дизайн екрана входу.**

   Необхідно створити базовий дизайн екрану для авторизації користувача.<br>
      Екран авторизації користувача повинний містити поле для вводу логіну та паролю. Також необхідно додати кнопку для підтвердження логіну.<br>

3. **Заняття з Intent**  
   1. **Створити початковий дизайн екрана профілю**  
      Необхідно створити додаткове Activity \-\> MainActivity.<br>
      Створити новий Layout файл \-\> activity\_main.<br>
      Створити базовий дизайн профілю користувача. Профіль користувача складається із:<br>
      зображення профілю (поставити фіксовану картинку),<br>
      ім'я користувача,<br>
      Опис користувача.<br>
   2. **Реалізувати перевірку введених даних (поля електронної пошти та пароля не повинні бути порожніми).**  
      Всередині AuthorizationActivity реалізувати базову логіку для перевірки введених даних в поля логіну та паролю (необхідно перевірити, чи поля не є пусті).<br>
   3. **Реалізувати перехід з Activity авторизації до MainActivity.**
   	У випадку, якщо користувач клікнув на кнопку Login та дані логіну і паролю є вірну, то зробити перехід із екрану AuthorizationActivity \-\> MainActivity.<br>

4. **Заняття з Fragment**  
   1. **Реалізувати базову логіку SignInFragment**  
      Перенести дизайн і логіку для валідації даних із AuthorizationActivity у новий фрагмент SignInFragment. Фрагмент повинний містити кнопки для реєстрації (Sign Up),  забув пароль (Forgot password).<br> 
      	У випадку кліку на Sign In організувати перехід на MainActivity. Також дописати внутрішні переходи між екранами при кліку на відповідні кнопки.<br>
   2. **Створити початковий дизайн екрана реєстрації.**
   Користувач може не мати спочатку профілю для авторизації, тому необхідно створити фрагмент для реєстрації (SignUpFragment). Фрагмент повинний містити поля для введення логіну, пошти та початкового паролю. Також необхідні кнопки для підтвердження Реєстрації (Sign Up),  перехід на екран логіну (Sign In), забув пароль (Forgot password).<br> 
      	Всередині SignUpFragment реалізувати базову логіку для перевірки коректності введених даних. Також у випадку кліку на Sign Up організувати перехід на MainActivity. Також дописати внутрішні переходи між екранами при кліку на відповідні кнопки.<br>

   3. **Створити початковий дизайн екрана відновлення пароля.**
   необхідно створити фрагмент для відновлення паролю (ForgotPasswordFragment). Фрагмент повинний містити поля для введення пошти. Також необхідні кнопки для підтвердження (Send new password).<br>
      	Всередині ForgotPasswordFragment реалізувати базову логіку для перевірки коректності введених даних. Також у випадку кліку на Send new password організувати перехід на LoginFragment.<br>

5. **Заняття з баз даних**  
   1. **Навчитися використовувати адаптери та RecyclerView**  
      Дослідити приклади використання Адаптерів. Вони будуть використовуватись надалі для відображення списків даних як, список постів, коментарів, альбомів та картинок.<br>
   2. **Реалізувати базовий ProfileFragment**  
      Перенести дизайн і логіку для валідації даних із MainActivity у новий фрагмент ProfileFragment.<br>
   3. **Реалізувати базове бокове меню NavigationDrawer**

   Приклад: [https://developer.android.com/training/implementing-navigation/nav-drawer.html](https://developer.android.com/training/implementing-navigation/nav-drawer.html) <br>

   Створити базове бокове меню. Воно буде використовуватись для навігації користувача між екранами (профіль, пости, альбоми і тд). <br>

6. **Заняття з роботи з мережею**  
   1. **Створити моделі даних Album та Image.**

   Необхідно створити класи моделі для відображення даних про альбом та картинки. Для цього необхідно створити вручну класи, які містять такі ж поля як і у прикладах:<br>

   Альбоми [http://jsonplaceholder.typicode.com/albums/1](http://jsonplaceholder.typicode.com/albums/1)<br>

   Фотографії [http://jsonplaceholder.typicode.com/photos/1](http://jsonplaceholder.typicode.com/photos/1)<br>

   2. **Реалізувати базові запити до API для отримання списку альбомів.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку albums. Реалізувати **AlbumRepository** із методами для завантаження всіх альбомів і конкретного альбому.<br>

   3. **Реалізувати базові запити до API для отримання списку зображень.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку images. Реалізувати **ImageRepository** із методами для завантаження всіх картинок у альбомі.<br>

   4. **Навчитися використовувати бібліотеку завантаження зображень Picasso або Glide.**
   Дослідити інтеграцію і роботу із бібліотеками для завантаження картинок.<br>

   5. **Реалізувати базовий AlbumsFragment**
   Реалізувати фрагмент, який містить список у якому відображається інформація про альбом.<br>

   6. **Реалізувати базовий ImagesFragment**
   Реалізувати фрагмент, який містить список у якому відображається таблиця із завантаженими картинками.<br>

7. **Заняття з файлів та SharedPreferences**  
   1. **Створити моделі даних Profile, Post та Comment.**
   Необхідно створити класи моделі для відображення даних про Профіль, пости та коменти. Для цього необхідно створити вручну класи, які містять такі ж поля як і у прикладах:<br>

   Профіль [http://jsonplaceholder.typicode.com/users/1](http://jsonplaceholder.typicode.com/users/1)<br>

   Допис [http://jsonplaceholder.typicode.com/posts/1](http://jsonplaceholder.typicode.com/posts/1)<br>

   Коментар [http://jsonplaceholder.typicode.com/comments/1](http://jsonplaceholder.typicode.com/comments/1)<br>

   2. **Реалізувати базові запити до API для отримання списку профілів.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку users. Реалізувати **ProfileRepository** із методами для завантаження всіх профілів і окремого профілю за заданим id.<br>

   3. **Реалізувати базові запити до API для отримання списку дописів.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку posts. Реалізувати **PostRepository** із методами для завантаження всіх постів і окремого посту за заданим id.<br>

   4. **Реалізувати базові запити до API для отримання списку коментарів.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку comments. Реалізувати **CommentRepository** із методами для завантаження всіх постів і окремого посту за заданим id.<br>

8. **Заняття з Service та AsyncTask**  
   1. **Реалізувати базовий PostsFragment**

   Реалізувати фрагмент, який містить список у якому відображається інформація про пости.<br>

   2. **Реалізувати базовий CommentsFragment**

   Реалізувати фрагмент, який містить список у якому відображається перелік коментів до заданого посту.<br>

9. **Заняття з датчиків**  
   1. **Створити модель даних Todo.**

   Необхідно створити класи моделі для відображення даних про todo. Для цього необхідно створити вручну клас, який містіть такі ж поля як і у прикладах:<br> 
   Завдання [http://jsonplaceholder.typicode.com/todos/1](http://jsonplaceholder.typicode.com/todos/1)<br>

   2. **Реалізувати базові запити до API для отримання списку завдань.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку todos. Реалізувати **TodoRepository** із методами для завантаження всіх todo.<br>

   3. **Реалізувати базовий TodoFragment**

   Реалізувати фрагмент, який містить список у якому відображається перелік todo.<br>

10. **Підсумкове заняття**  
    1. **Завершити розробку застосунку.**
    Завершити додаток та виправити помилки.<br>
