Module simpleusers.users
========================

Classes
-------

`usermgr()`
:   A class for managing user data and authentication.
    
    Attributes:
        srcdir (str): The directory where user data is stored.
    
    Initializes the UserManager instance.
    
    Creates the data directory if it doesn't exist.

    ### Methods

    `auth_user(self, uid, attempt)`
    :   Authenticates a user.
        
        Args:
            uid (str): User ID or filename.
            attempt (str): Password attempt for authentication.
        
        Returns:
            bool: True if authentication is successful, False otherwise.

    `check_user_exists(self, uid)`
    :   Checks if a user exists.
        
        Args:
            uid (str): User ID or filename.
        
        Returns:
            bool: True if the user exists, False otherwise.

    `dump_users(self)`
    :   Lists the users in the data directory.
        
        Returns:
            list: List of user filenames.

    `get_user(self, uid)`
    :   Retrieves user data from a YAML file.
        
        Args:
            uid (str): User ID or filename.
        
        Returns:
            dict: User data as a dictionary.

    `make_user(self, uid, passw)`
    :   Creates a new user.
        
        Args:
            uid (str): User ID or filename.
            passw (str): User password.
        
        Returns:
            None

    `set_user_password(self, uid, newpass)`
    :   Sets a new password for a user.
        
        Args:
            uid (str): User ID or filename.
            newpass (str): New password.
        
        Returns:
            dict: Result message.

    `set_user_prop(self, uid, key, val)`
    :   Sets a property for a user.
        
        Args:
            uid (str): User ID or filename.
            key (str): Property key.
            val: Property value.
        
        Returns:
            dict: Result message.

    `write_user(self, uid, obj)`
    :   Writes user data to a YAML file.
        
        Args:
            uid (str): User ID or filename.
            obj (dict): User data as a dictionary.
        
        Returns:
            None