# Задача 1
1. auth - микрофронтенд аутентификации/авторизации пользователя, отвечает за входом/регистрацию в сервис
2. profile микрофронтенд редактирования профиля пользователя, его аватара
3. places микрофронтенд отвечает за лайки/дизлайки, карточки мест
4. host микрофронтенд главный микрофронтенд, тут собрана компоновка приложения, пользовательский контекст

В данном проекте предлагаю использовать ModuleFederation поскольку:
1. В данном приложении не требуется ни в одном микрофронтенде использовать фреймворк отличный от react
2. Он более прост в настройке
3. В ModuleFederation действует модульная система, благодаря, которой можно независимым приложениям использовать общий код
Хотя для более крупного быстро развивающегося монолита я бы предложил SingleSpa - независимость фреймоврков, изолированный процесс развертывания
```
/auth
  /src
    /components
      Login.js           
      Register.js    
    /styles
      /auth-form
        ...
      /login 
        ...
    /utils
      auth.js                
    index.js     
  package.json      
  webpack.config.js
/profile
  /src
    /components
      EditAvatarPopup.js           
      EditProfilePopup.js   
      PopupWithForm.js    
    /styles
      /popup
        ...
      /profile
        ...  
      /page
        ...        
    /utils
      api.js
    /images
       ...                    
    index.js     
  package.json      
  webpack.config.js
/places
  /src
    /components
      AddPlacePopup.js           
      Card.js   
      ImagePopup.js    
      PopupWithForm.js
    /styles
      /card
        ...
      /places
        ...  
      /popup
        ...       
    /utils
      api.js                 
    index.js   
    /images
       ...  
  package.json      
  webpack.config.js  
/host
  /src
    /components
      App.js           
      Footer.js   
      Header.js  
      Main.js
      InfoTooltip.js
      ProtectedRoute.js  
    /styles
      /footer
        ...
      /header
        ... 
      /content
        ...  
      /images
        ...  
    /contexts
      CurrentUserContext.js                    
    index.js     
  package.json      
  webpack.config.js   
```
# Задача 2
https://drive.google.com/file/d/1yedI8RZbUSkkD7PhbcMUeZqSqShios8l/view?usp=sharing
