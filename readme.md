# Session #1: How to create the base for your site
## 1. Create the project

Create a new project by running the following command:

`
composer create-project symfony/website-skeleton projet-de-certification
`

Aller dans le dossier de votre projet projet-de-certification (placez-vous dedans)

`
composer require symfony/web-server-bundle --dev ^4.4.16
`

Start the project to view it in the browser:

`
php bin/console server:run
`

## 2. Make a homepage

Make a homepage by running the following command which create a new controller class:

`
php bin/console make:controller
`

## 3. Make a contact page

Make a contact page by running the following command which create a new controller class:

`
php bin/console make:controller
`

Add a form so that the user can input a message to send:

```
$form = $this->createFormBuilder()
    ->add('from', EmailType::class)
    ->add('name', TextType::class)
    ->add('message', TextareaType::class)
    ->add('send', SubmitType::class)
    ->getForm();

return $this->render('contact/index.html.twig', [
    'controller_name' => 'ContactController',
    'contact_form' => $form->createView(),
]);
```

Display this form in the twig file (templates/contact/index.html.twig) (if you don't add this line, you won't see the form):

```
{{ form(contact_form) }}
```

## 4. Creating login form

`
php bin/console make:user
`

`
php bin/console make:auth
`

## 5. Setup database
Create yesman database with phpmyadmin

Change the DATABASE_URL in the .env file so that Symfony can connect

Then, order Symfony to connect to the database and create all necessary tables for you:

`
php bin/console make:migration
`

`
php bin/console doctrine:migrations:migrate
`

## 6. Create registration form

Create the registration form with the following command:

`
php bin/console make:registration-form
`

## 7. Adding a valid redirect

Change the file LoginFormAuthenticator.php in src/Security to tell Symfony what page is the homepage after login:

```
return new RedirectResponse($this->urlGenerator->generate('home'));
```

## 8. Adding bootstrap

Go to the official bootstrap website and add all the necessary links to the base.twig.html

Tell Symfony to apply the bootstrap style for every page of the application (file: config/packages/twig.yaml)

```
form_themes: ['bootstrap_4_horizontal_layout.html.twig']
```

# Session #2: How to style your pages with bootstrap

## 1. Create all the pages

Create all your pages with the following command. Create 1 controller per page: create 1 controller for each of your page:

`
php bin/console make:controller
`

## 2. Style your page with bootstrap

Important BOOTSTRAP CLASSES (class="...") to know are:
- container : it's a page container, with spacing around it
```
<div class="container"></div>
``` 

- row : to create a row
```
<div class="container">
    <div class="row">
    </div>
</div>
``` 

- col : to create columns INSIDE a row
```
<div class="container">
    <div class="row">
        <div class="col"></div>
        <div class="col"></div>
    </div>
</div>
``` 

- w-100 : to force the width to be 100% of the parent's
```
<div class="container">
    <div class="row">
        <div class="col">
            <img src="image.jpg" class="w-100" />
        </div>
        <div class="col"></div>
    </div>
</div>
``` 

Play around with bootstrap! Have fun and make your page sexy!