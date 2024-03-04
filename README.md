## Create the enviroment and install dependencies

```
python -m venv en
source env/bin/activate
pip install -r "requirements.txt"
```

## Seed the database
```
export FLASK_APP=app
```
```
flask shell
```

```
from app import db, Post
db.create_all()

post_1 = Post(title='How to create a blog', content='In this tutorial we are going to create a blog')

post_2 = Post(title='How to create a website', content='In this tutorial we are going to create a website')

post_3 = Post(title='Build a webpage by yourself', content='In this tutorial we are going to create a webpage')

post_4 = Post(title='Python tutorial', content='python content')
post_5 = Post(title='Java tutorial', content='python content')
post_6 = Post(title='Ruby tutorial', content='python content')

db.session.add(post_1)
db.session.add(post_2)
db.session.add(post_3)
db.session.add(post_4)
db.session.add(post_5)
db.session.add(post_6)
db.session.commit()
```

Check if the posts have been inserted.
```
Post.query.all()
```

# Run the app

```
export FLASK_APP=app
export FLASK_ENV=development
```

```
flask --debug run
```
