Stworzenie App Service
![App Service](https://user-images.githubusercontent.com/48619944/116151195-96577380-a6e4-11eb-8476-9911bc1de6d1.png)

Wdrożenie aplikacji na platformie Azure

1. Zmiena pliku deploymentu app-name: '##appname##' slot-name: 'production' publish-profile: ${{ secrets.AZURE_WEBAPP_PUBLISH_PROFILE }} package: .

2. Dodanie nowego secretu o nazwie AZURE_WEBAPP_PUBLISH_PROFILE, jako wartość należy dodać pobrane informacje z Azure publish Profile
![2](https://user-images.githubusercontent.com/48619944/116135901-f690ea00-a6d1-11eb-85cb-9d3fc0f7058e.png)

3. Deploy aplikacji przez Github Actions 
![3](https://user-images.githubusercontent.com/48619944/116135905-f7c21700-a6d1-11eb-810d-0b0b52d0e4d8.png)

4. W AppService Azura w Konfiguracji należy dodać 2 ustawienia aplikacji NODE_CONFIG oraz NODE_ENV
![Kod wstawienie](https://user-images.githubusercontent.com/48619944/116151690-37462e80-a6e5-11eb-89cf-0a64fe9b493c.png)
![4](https://user-images.githubusercontent.com/48619944/116135909-f7c21700-a6d1-11eb-8197-4459e9e5e315.png)
![5](https://user-images.githubusercontent.com/48619944/116135914-f98bda80-a6d1-11eb-907a-48ecaec1cb87.png)

5. Stworzono bazę danych CosmoDB oraz uzupełniamy connection string 
![5 1](https://user-images.githubusercontent.com/48619944/116136138-38219500-a6d2-11eb-9008-40625051edde.png)

6. Po wgraniu i skonfigurowaniu aplikacja wysyła requestowane maile
![6](https://user-images.githubusercontent.com/48619944/116135921-fb559e00-a6d1-11eb-8999-0a2a219b0e0e.png)

#########################################################################
Post /v1/user
![7](https://user-images.githubusercontent.com/48619944/116135923-fc86cb00-a6d1-11eb-9dae-0cc5a9ca4cd1.png)

Get /v1/user 
![8](https://user-images.githubusercontent.com/48619944/116135926-fdb7f800-a6d1-11eb-913f-74bdc450e361.png)

Get /v1/mail 
![9](https://user-images.githubusercontent.com/48619944/116135931-fee92500-a6d1-11eb-89d1-c9eae9a0fbbf.png)

Post /v1/mail 
![10](https://user-images.githubusercontent.com/48619944/116135937-ff81bb80-a6d1-11eb-91a3-89aee4e9dea4.png)
