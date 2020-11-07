# Start the project
Create a new project by running the following command:

`
composer create-project symfony/website-skeleton yesman
`

Aller dans le dossier de votre projet yesman (placez dedans)

`
composer require symfony/web-server-bundle --dev ^4.4.16
`

Start the project to view it in the browser:

`
php bin/console server:run
`

# Make a homepage

Make a homepage by running the following command which create a new controller class:

`
php bin/console make:controller
`

# Make a contact page

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

Display this form in the twig file (if you don't display it, you won't see the form)

`
{{ form(contact_form) }}
`

# Creating login form

`
php bin/console make:user
`

`
php bin/console make:auth
`

# Setup database
Create yesman database with phpmyadmin

Change the DATABASE_URL in the .env file so that Symfony can connect

Then, order Symfony to connect to the database and create all necessary tables for you:

`
php bin/console make:migration
`

`
php bin/console doctrine:migrations:migrate
`

# Create registration form

Create the registration form with the following command:

`
php bin/console make:registration-form
`

# Adding a valid redirect

Change the file LoginFormAuthenticator.php in src/Security to tell Symfony what page is the homepage after login:

```
return new RedirectResponse($this->urlGenerator->generate('home'));
```

# Adding bootstrap

Go to the official bootstrap website and add all the necessary links to the base.twig.html

Tell Symfony to apply the bootstrap style for every page of the application

`
form_themes: ['bootstrap_4_horizontal_layout.html.twig']
`