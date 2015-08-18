Survey Monkey evidently doesn't support a basic tool of data scientists: That of summing values per section.

For example, imagine responses in which we want to group colors together and tastes together.

    Name,Red?,Blue?,Age,Sweet?,Sour?
    Chad,sometimes,sometimes,100,always,always
    Ben,never,sometimes,100,never,always

My program changes it,
if you specify group ranges "2-3,5,6", and
answering "never" means 0, and
"sometimes" means 1, and 
"always" means 2,
to

    Name,Red?,Blue?,group 1 sum,Age,Sweet?,Sour?,group 2 sum
    Chad,sometimes,sometimes,100,2,always,always,4
    Ben,never,sometimes,100,1,never,always,2
