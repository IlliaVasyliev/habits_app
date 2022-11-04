# habits_app

## Installation and Testing

if you want to install app run following commands:

1. Install Dependencies

```console
pip install -r requirements.txt
```

2. Perform database migrations and start server (instead of python you may need to type python2 or python3 depending on the machine)

```console
python manage.py migrate
python manage.py runserver
```

3. for testing you can run this command (instead of python you may need to type python2 or python3 depending on the machine)

```console
python manage.py test
```

- Test Dataset is stored in `./habits/mock_data.py`


# Examples of requsts to service (how to interact with system)

You can create and run them in postman

### API Endpoints

| Endpoints                       | Response Body Parameters                                                         | Actions                                |
| ------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------- |
| /habits/create_user             | username (string)                                                                | To set up a new user account           |
| /habits/create_habit            | habit_name (string), periodicity(string, either 'DAY' or 'WEEK', default= 'DAY') | To create a new habit                  |
| /habits/add_user_for_habit | user_id (int), habit_id (int)                                                    | To register habit to the user          |
| /habits/perform_habit        | user_id (int), habit_id(int), submit_date (Date %Y-%m-%d)                        | To record habit action |
| /habits/get_user_info           | user_id (int) | To retrieve details of the user                                            |
| /habits/get_habit_score         | habit_id (int) | To retrieve habits rating                                            |
