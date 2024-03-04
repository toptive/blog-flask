## Create the enviroment and install dependencies

Create an enviroment (optional)
```
python -m venv env
source env/bin/activate
```

Install dependencies
```
pip install -r "requirements.txt"
```

## DB setup

```
export FLASK_APP=app
flask shell
```

Create the database
```
from app import db, Post
db.create_all()
```

Add posts
```
post_1 = Post(title='How to create a blog', content='In this tutorial we are going to create a blog')
post_2 = Post(title='How to create a website', content='In this tutorial we are going to create a website')
post_3 = Post(title='Build a webpage by yourself', content='In this tutorial we are going to create a webpage')
post_4 = Post(title='Python tutorial', content='python tutorial content')
post_5 = Post(title='Java tutorial', content='java tutorial content')
post_6 = Post(title='Ruby tutorial', content='ruby tutorial content')

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

# Install npm dependencies
```
npm install
```

# Run tailwindcss build process
```
npm run create-css
```

# Run the flask app
```
export FLASK_APP=app
export FLASK_ENV=development
flask --debug run
```
