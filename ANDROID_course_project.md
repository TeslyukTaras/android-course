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

   На даному етапі необхідно встановити AndroidStudio та створити новий проект.<br>
      Ім”я пакету варто вибрати наступним чином:<br>

   сom.pllug.course.ваше прізвище англійською мовою і маленькими символами.<br>

   Вказати назву Activity \-\> **AuthorizationActivity**.

   Вказати назву Layout \-\> **activity\_authorization**.

2. **View lesson**  
   1. **Create initial design for login screen.**

   Необхідно створити базовий дизайн екрану для авторизації користувача.<br>
      Екран авторизації користувача повинний містити поле для вводу логіну та паролю. Також необхідно додати кнопку для підтвердження логіну.<br>

3. **Intent lesson**  
   1. **Create initial design for Profile screen**  
      Необхідно створити додаткове Activity \-\> MainActivity.<br>
      Створити новий Layout файл \-\> activity\_main.<br>
      Створити базовий дизайн профілю користувача. Профіль користувача складається із:<br>
      зображення профілю (поставити фіксовану картинку),<br>
      ім'я користувача,<br>
      Опис користувача.<br>
   2. **Implement user input validation logic (email, password are not empty).**  
      Всередині AuthorizationActivity реалізувати базову логіку для перевірки введених даних в поля логіну та паролю (необхідно перевірити, чи поля не є пусті).<br>
   3. **Implement logic to move from Authorization activity to MainActivity.**
   	У випадку, якщо користувач клікнув на кнопку Login та дані логіну і паролю є вірну, то зробити перехід із екрану AuthorizationActivity \-\> MainActivity.<br>

4. **Fragment lesson**  
   1. **Implement basic logic for SignInFragment**  
      Перенести дизайн і логіку для валідації даних із AuthorizationActivity у новий фрагмент SignInFragment. Фрагмент повинний містити кнопки для реєстрації (Sign Up),  забув пароль (Forgot password).<br> 
      	У випадку кліку на Sign In організувати перехід на MainActivity. Також дописати внутрішні переходи між екранами при кліку на відповідні кнопки.<br>
   2. **Create initial design for sign up screen.**
   Користувач може не мати спочатку профілю для авторизації, тому необхідно створити фрагмент для реєстрації (SignUpFragment). Фрагмент повинний містити поля для введення логіну, пошти та початкового паролю. Також необхідні кнопки для підтвердження Реєстрації (Sign Up),  перехід на екран логіну (Sign In), забув пароль (Forgot password).<br> 
      	Всередині SignUpFragment реалізувати базову логіку для перевірки коректності введених даних. Також у випадку кліку на Sign Up організувати перехід на MainActivity. Також дописати внутрішні переходи між екранами при кліку на відповідні кнопки.<br>

   3. **Create initial design for forgot password screen.**
   необхідно створити фрагмент для відновлення паролю (ForgotPasswordFragment). Фрагмент повинний містити поля для введення пошти. Також необхідні кнопки для підтвердження (Send new password).<br>
      	Всередині ForgotPasswordFragment реалізувати базову логіку для перевірки коректності введених даних. Також у випадку кліку на Send new password організувати перехід на LoginFragment.<br>

5. **Databases lesson**  
   1. **Learn how to use Adapters and RecyclerView**  
      Дослідити приклади використання Адаптерів. Вони будуть використовуватись надалі для відображення списків даних як, список постів, коментарів, альбомів та картинок.<br>
   2. **Implement basic ProfileFragment**  
      Перенести дизайн і логіку для валідації даних із MainActivity у новий фрагмент ProfileFragment.<br>
   3. **Implement basic NavigationDrawer**

   Приклад: [https://developer.android.com/training/implementing-navigation/nav-drawer.html](https://developer.android.com/training/implementing-navigation/nav-drawer.html) <br>

   Створити базове бокове меню. Воно буде використовуватись для навігації користувача між екранами (профіль, пости, альбоми і тд). <br>

6. **Networking lesson**  
   1. **Create data models for Album and Image.**

   Необхідно створити класи моделі для відображення даних про альбом та картинки. Для цього необхідно створити вручну класи, які містять такі ж поля як і у прикладах:<br>

   Albums [http://jsonplaceholder.typicode.com/albums/1](http://jsonplaceholder.typicode.com/albums/1)<br>

   Photos [http://jsonplaceholder.typicode.com/photos/1](http://jsonplaceholder.typicode.com/photos/1)<br>

   2. **implement basic api calls to get list of albums.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку albums. Реалізувати **AlbumRepository** із методами для завантаження всіх альбомів і конкретного альбому.<br>

   3. **implement basic api calls to get list of images.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку images. Реалізувати **ImageRepository** із методами для завантаження всіх картинок у альбомі.<br>

   4. **Learn how to use Picasso or Glide image loading library.**
   Дослідити інтеграцію і роботу із бібліотеками для завантаження картинок.<br>

   5. **Implement basic AlbumsFragment**
   Реалізувати фрагмент, який містить список у якому відображається інформація про альбом.<br>

   6. **Implement basic ImagesFragment**
   Реалізувати фрагмент, який містить список у якому відображається таблиця із завантаженими картинками.<br>

7. **Files, Shared preferences lesson**  
   1. **Create data models for Profile, Post and Comment.**
   Необхідно створити класи моделі для відображення даних про Профіль, пости та коменти. Для цього необхідно створити вручну класи, які містять такі ж поля як і у прикладах:<br>

   Profile [http://jsonplaceholder.typicode.com/users/1](http://jsonplaceholder.typicode.com/users/1)<br>

   Post [http://jsonplaceholder.typicode.com/posts/1](http://jsonplaceholder.typicode.com/posts/1)<br>

   Comment [http://jsonplaceholder.typicode.com/comments/1](http://jsonplaceholder.typicode.com/comments/1)<br>

   2. **implement basic api calls to get list of profiles.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку users. Реалізувати **ProfileRepository** із методами для завантаження всіх профілів і окремого профілю за заданим id.<br>

   3. **implement basic api calls to get list of posts.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку posts. Реалізувати **PostRepository** із методами для завантаження всіх постів і окремого посту за заданим id.<br>

   4. **implement basic api calls to get list of comments.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку comments. Реалізувати **CommentRepository** із методами для завантаження всіх постів і окремого посту за заданим id.<br>

8. **Service AsyncTask lesson**  
   1. **Implement basic PostsFragment**

   Реалізувати фрагмент, який містить список у якому відображається інформація про пости.<br>

   2. **Implement basic CommentsFragment**

   Реалізувати фрагмент, який містить список у якому відображається перелік коментів до заданого посту.<br>

9. **Sensors lesson**  
   1. **Create data model for Todo.**

   Необхідно створити класи моделі для відображення даних про todo. Для цього необхідно створити вручну клас, який містіть такі ж поля як і у прикладах:<br> 
   Todo [http://jsonplaceholder.typicode.com/todos/1](http://jsonplaceholder.typicode.com/todos/1)<br>

   2. **implement basic api calls to get list of todos.**

   Використати бібліотеку **Retrofit** для виконання запитів для завантаження переліку todos. Реалізувати **TodoRepository** із методами для завантаження всіх todo.<br>

   3. **Implement basic TodoFragment**

   Реалізувати фрагмент, який містить список у якому відображається перелік todo.<br>

10. **Final lesson**  
    1. **Finalize your application.**
    Завершити додаток та виправити помилки.<br>