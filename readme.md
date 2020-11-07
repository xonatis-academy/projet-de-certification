# Start the project
composer create-project symfony/website-skeleton yesman
-> aller dans le dossier de votre projet yesman (placez dedans)
composer require symfony/web-server-bundle --dev ^4.4.16
php bin/console server:run

# Make a home page
php bin/console make:controller

# Make a contact page
php bin/console make:controller

`
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
`

`
{{ form(contact_form) }}
`

# Creating login form
php bin/console make:user
php bin/console make:auth

# Setup database
create yesman database
change .env file
php bin/console make:migration
php bin/console doctrine:migrations:migrate

# Create registration form
php bin/console make:registration-form

# Adding a valid redirect
`
return new RedirectResponse($this->urlGenerator->generate('home'));
`

# Adding bootstrap
Go to the official bootstrap website
`
form_themes: ['bootstrap_4_horizontal_layout.html.twig']
`