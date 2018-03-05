# Installing Pip and SQLite3

```
sudo apt install python3-pip sqlite3
```

# Installing dependencies

```
sudo pip3 install Django sqlparse tqdm uwsgi markdown virtualenv
```

# Setting up

```
chmod a+x ./scripts/*
./scripts/setup
./scripts/seed
```

# Clear the databse

```
sqlite3 db.sqlite3
delete from annotator_video;
delete from sqlite_sequence where name='annotator_video';
```

# Running the server

```
./scripts/serve
```

# Open Browser

Go to address 0.0.0.0:5000/admin
(username: test, password: password)

# Add Labels

Go to 0.0.0.0:5000/admin/annotator/label/
Click on the top right button 'ADD LABEL'
Enter appropriate Name and any 6digit color code (000000 should be good enough)
Save

# Add State

Go to 0.0.0.0:5000/admin/annotator/state/
Click on the top right button 'ADD STATE'
Enter appropriate Name and ,6digit color code (000000 should be good enough) and select the corresponding label name
Save

# Add video

Go to 0.0.0.0:5000/admin/annotator/video/
Click on the top right button 'ADD VIDEO'
Enter:
    Source: Appropriate name (e.g. Sharpner)
    Filename: Name of the file (e.g. 0018.mp4)
    Host: /static/videos/
Save

# Go to video

Go to 0.0.0.0:5000/admin/annotator/video/
Click on the video you want to annotate
Annotate the video
Save


# Index

Labels
1. mug1
2. mug2 
3. notepad
4. sunglass
5. stapler
6. clip1
7. clip2
8. clip3
9. pen
10. calculator
11. stapler
12. sharpener
13. ball
14. bottle1
15. bottle2

mug1 = flower design mug
mug2 = red mug
clip1 = yellow clip
clip2 = red clip
clip3 = black clip
bottle1 = coke bottle
bottle2 = amul cool bottle
notepad = stickypad
