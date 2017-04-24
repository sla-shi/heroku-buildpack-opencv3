# Heroku Buildpack for OpenCV3 and Python 3.6

This buildpack is based on the VM image described in 
https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b

# Adding buildpack

This buildpack requires heroku/python (python 3.6 runtime) buildpack already added to your heroku app. 
You will need to add runtime.txt with the following content to your app repository:
```
python-3.6.1
```

Add another buildpack (OpenCV): 

```
heroku config:add --index=2 BUILDPACK_URL=https://github.com/sla-shi/heroku-buildpack-opencv3.git
```

Deploy your app

```
git push heroku master
```

# Thanks
Many thanks to Adam Geitgey who saved me hours by providing ready to use VM image with OpenCV3 preinstalled.
