<?php
try {
    $user->login();
}  catch (AuthenticationFailureException $e) {
    set_error_handler("my_login_form_handler");
    trigger_error("User could not be logged in. Please check username and password and try again!");
} catch (PersistenceException $pe) { // database unavailable
    set_error_handler("my_login_form_handler"); 
    trigger_error("Internal system error. Please contact the administrator.");
}
