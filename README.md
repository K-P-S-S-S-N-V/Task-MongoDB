<div align="center">
  <h1><code>Queries Answering & CRUD Operations Using Python MongoDB</code></h1>

  <p>
    <strong>Task by 
    <a href="https://www.guvi.in/">GUVI - Greek Networks</a></strong>
  </p>

  <strong>A <a href="https://www.mongodb.com/docs/drivers/pymongo/">Pymongo</a> project</strong>
  <h3>
    <strong> A Simple
    <a href="https://www.mongodb.com/languages/python/pymongo-tutorial">Guide </a> by Mongodb.com</strong>
   
  </h3>
</div>

## Task-MongoDB
This is the code to Run MongoDB Server On Google Colaboratory and answering the Queries related to Available student.json Dataset from MongoDB.


## First Install " dnspython " and " pymongo server " in Google Colaboratory
```python
!apt install mongodb
!service mongodb start
```
Output:
```
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following package was automatically installed and is no longer required:
  libnvidia-common-460
Use 'apt autoremove' to remove it.
The following additional packages will be installed:
  libpcap0.8 libstemmer0d libyaml-cpp0.5v5 mongo-tools mongodb-clients
  mongodb-server mongodb-server-core
The following NEW packages will be installed:
  libpcap0.8 libstemmer0d libyaml-cpp0.5v5 mongo-tools mongodb mongodb-clients
  mongodb-server mongodb-server-core
0 upgraded, 8 newly installed, 0 to remove and 29 not upgraded.
Need to get 53.1 MB of archives.
After this operation, 215 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 libpcap0.8 amd64 1.8.1-6ubuntu1.18.04.2 [118 kB]
Get:2 http://archive.ubuntu.com/ubuntu bionic/main amd64 libstemmer0d amd64 0+svn585-1build1 [62.5 kB]
Get:3 http://archive.ubuntu.com/ubuntu bionic/universe amd64 libyaml-cpp0.5v5 amd64 0.5.2-4ubuntu1 [150 kB]
Get:4 http://archive.ubuntu.com/ubuntu bionic/universe amd64 mongo-tools amd64 3.6.3-0ubuntu1 [12.3 MB]
Get:5 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-clients amd64 1:3.6.3-0ubuntu1.4 [20.2 MB]
Get:6 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-server-core amd64 1:3.6.3-0ubuntu1.4 [20.3 MB]
Get:7 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-server all 1:3.6.3-0ubuntu1.4 [12.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb amd64 1:3.6.3-0ubuntu1.4 [10.2 kB]
Fetched 53.1 MB in 1s (61.0 MB/s)
Selecting previously unselected package libpcap0.8:amd64.
(Reading database ... 123942 files and directories currently installed.)
Preparing to unpack .../0-libpcap0.8_1.8.1-6ubuntu1.18.04.2_amd64.deb ...
Unpacking libpcap0.8:amd64 (1.8.1-6ubuntu1.18.04.2) ...
Selecting previously unselected package libstemmer0d:amd64.
Preparing to unpack .../1-libstemmer0d_0+svn585-1build1_amd64.deb ...
Unpacking libstemmer0d:amd64 (0+svn585-1build1) ...
Selecting previously unselected package libyaml-cpp0.5v5:amd64.
Preparing to unpack .../2-libyaml-cpp0.5v5_0.5.2-4ubuntu1_amd64.deb ...
Unpacking libyaml-cpp0.5v5:amd64 (0.5.2-4ubuntu1) ...
Selecting previously unselected package mongo-tools.
Preparing to unpack .../3-mongo-tools_3.6.3-0ubuntu1_amd64.deb ...
Unpacking mongo-tools (3.6.3-0ubuntu1) ...
Selecting previously unselected package mongodb-clients.
Preparing to unpack .../4-mongodb-clients_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb-clients (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb-server-core.
Preparing to unpack .../5-mongodb-server-core_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb-server-core (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb-server.
Preparing to unpack .../6-mongodb-server_1%3a3.6.3-0ubuntu1.4_all.deb ...
Unpacking mongodb-server (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb.
Preparing to unpack .../7-mongodb_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb (1:3.6.3-0ubuntu1.4) ...
Setting up libstemmer0d:amd64 (0+svn585-1build1) ...
Setting up libyaml-cpp0.5v5:amd64 (0.5.2-4ubuntu1) ...
Setting up mongodb-server-core (1:3.6.3-0ubuntu1.4) ...
Setting up libpcap0.8:amd64 (1.8.1-6ubuntu1.18.04.2) ...
Setting up mongodb-clients (1:3.6.3-0ubuntu1.4) ...
Setting up mongodb-server (1:3.6.3-0ubuntu1.4) ...
invoke-rc.d: could not determine current runlevel
invoke-rc.d: policy-rc.d denied execution of start.
Created symlink /etc/systemd/system/multi-user.target.wants/mongodb.service → /lib/systemd/system/mongodb.service.
Setting up mongo-tools (3.6.3-0ubuntu1) ...
Setting up mongodb (1:3.6.3-0ubuntu1.4) ...
Processing triggers for systemd (237-3ubuntu10.56) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
Processing triggers for libc-bin (2.27-3ubuntu1.6) ...
 * Starting database mongodb
   ...done.
```
## Insert Data
```python
x=records2.insert_many(data)           #to insert no.of available data in student.json file
print(x.inserted_ids)                  #print to see what are the ID's that are available for student data in student.json file
```
Output:
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199]
```
## To Count uploaded Record
```python
records2.count_documents({})      #Code to check how many total students are available 
```
Output:
```
200
```
##  To find Start data
```python
records2.find_one()      #to find Student data
```
Output:
(From student.json file)
```
{'_id': 0,
 'name': 'aimee Zank',
 'scores': [{'score': 1.463179736705023, 'type': 'exam'},
  {'score': 11.78273309957772, 'type': 'quiz'},
  {'score': 35.8740349954354, 'type': 'homework'}]}
```

## Now Let us Answer to the Questions

# 1) Find the student name who scored maximum scores in all (exam, quiz and homework)?
## student who score highest score in exam
```python
db = client.test
exam=db.exam_collection              #Total no.of Exam documents count 
exam.count_documents({})
```
Output:
```
200
```
```python
exam.drop()

for j in range(200):
  x=records2.aggregate([{"$match":{"_id":j}},{"$unwind":"$scores"},{"$match":{"scores.type":"exam"}},{"$sort":{"scores.score":-1}}])
  for i in x:
    i=exam.insert_many([i])

s=exam.find().sort('scores.score',-1).limit(1) 
for i in s:
  print(i)                              
```
Output:
```
{'_id': 136, 'name': 'Margart Vitello', 'scores': {'score': 99.33685767140612, 'type': 'exam'}}
```
## student who score highest score in quiz
```python
db = client.test
quiz=db.quiz_collection
quiz.count_documents({})                         #Total no.of Quiz documents count 
```
Output:
```
200
```
```python
quiz.drop()

for j in range(200):
  x=records2.aggregate([{"$match":{"_id":j}},{"$unwind":"$scores"},{"$match":{"scores.type":"quiz"}},{"$sort":{"scores.score":-1}}])
  for i in x:
    i=quiz.insert_many([i])

s=quiz.find().sort('scores.score',-1).limit(1)
for i in s:
  print(i)                               
```
Output:
```
{'_id': 69, 'name': 'Cody Strouth', 'scores': {'score': 99.80348240553108, 'type': 'quiz'}}
```
## student who score highest score in homework
```python
db = client.test
homework=db.homework_collection
homework.count_documents({})                     #Total no.of Homwwork documents counts 
```
Output:
```
200
```
```python
homework.drop()

for j in range(200):
  x=records2.aggregate([{"$match":{"_id":j}},{"$unwind":"$scores"},{"$match":{"scores.type":"homework"}},{"$sort":{"scores.score":-1}}])
  for i in x:
    i=homework.insert_many([i])
   
s=homework.find().sort('scores.score',-1).limit(1)
for i in s:
  print(i)                                #student who score highest score in homework
```
Output:
```
{'_id': 178, 'name': 'Whitley Fears', 'scores': {'score': 99.77237745070993, 'type': 'homework'}}
```
so, from here,
we got know about

## max score in exam is 'Margart Vitello'
{'_id': 136, 'name': 'Margart Vitello', 'scores': {'score': 99.33685767140612, 'type': 'exam'}}

## max score in quiz s 'Cody Strouth'
{'_id': 69, 'name': 'Cody Strouth', 'scores': {'score': 99.80348240553108, 'type': 'quiz'}}

## max score in homework is 'Whitley Fears'
{'_id': 178, 'name': 'Whitley Fears', 'scores': {'score': 99.77237745070993, 'type': 'homework'}}


# 2)Find students who scored below average in the exam and pass mark is 40%?

## first we need to find Avg score in Exam
```python

x=db.exam_collection.aggregate([{'$group' : {'_id' : "null", "avg_exam" : {'$avg' : "$scores.score"}}}])
for i in x:
  print(i)
```
Output:
```
{'_id': 'null', 'avg_exam': 48.67367075950175}
```
```python
db = client.test
lessavg=db.lessavg_collection
lessavg.count_documents({})  # total find no.of students with lessavg score  
```
Output:
```
104
```
## To find less than/ below average score in Exam
```python
lessavg.drop()

x=db.exam_collection.find({'scores.score':{'$lt':48.67367075950175} })
for i in x:
  i=lessavg.insert_many([i])
  
lessavg.count_documents({})
```
Output:
```
104
```

# 3) Find students who scored below pass mark and assigned them as fail, and above pass mark as pass in all the categories.

## Students who Fail in EXAM
```python
db = client.test
failexam=db.fail_exam
failexam.count_documents({})
```
Output:
```
81
```
```python
failexam.drop()

x=db.exam_collection.find(
    {'scores.score':{'$lt':40}
     }
)
for i in x:
  i=failexam.insert_many([i])
  #print(i)
  
failexam.count_documents({})
```
Output:
```
81
```
## Students who Pass in EXAM
```python
db = client.test
passexam=db.pass_exam
passexam.count_documents({})
```
Output:
```
119
```
```python
passexam.drop()

x=db.exam_collection.find(
    {'scores.score':{'$gte':40}
     }
)
for i in x:
  i=passexam.insert_many([i])

passexam.count_documents({})
```
Output:
```
119
```
## Students who Fail in Quiz
```python
db = client.test
failquiz=db.fail_quiz
failquiz.count_documents({})
```
Output:
```
86
```
```python
failquiz.drop()

x=db.quiz_collection.find(
    {'scores.score':{'$lt':40}
     }
)
for i in x:
  i=failquiz.insert_many([i])

failquiz.count_documents({})
```
Output:
```
86
```
## Students who Pass in Quiz
```python
db = client.test
passquiz=db.pass_quiz
passquiz.count_documents({})
```
Output:
```
114
```
```python
passquiz.drop()

x=db.quiz_collection.find(
    {'scores.score':{'$gte':40}
     }
)
for i in x:
  i=passquiz.insert_many([i])

passquiz.count_documents({})
```
Output:
```
114
```
## Students who fail in Homework
```python
db = client.test
failhomework=db.fail_homework
failhomework.count_documents({})
```
Output:
```
29
```
```python
failhomework.drop()

x=db.homework_collection.find(
    {'scores.score':{'$lt':40}
     }
)
for i in x:
  i=failhomework.insert_many([i])
  
  
failhomework.count_documents({})
```
Output:
```
29
```
## Students who Pass Home work
```python
db = client.test
passhomework=db.pass_homework
passhomework.count_documents({})
```
Output:
```
171
```
```python
passhomework.drop()

x=db.homework_collection.find(
    {'scores.score':{'$gte':40}
     }
)
for i in x:
  i=passhomework.insert_many([i])
  
passhomework.count_documents({})
```
Output:
```
171
```
Now Here,

db.fail_exam, db.fail_quiz, db.fail_homework....shows who scored below passmark and assingned the collection as fail in all the categories
db.pass_exam, db.pass_quiz, db.pass_homework....shows who scored above passmark and assingned the collection as pass in all the categories

# 4) Find the total and average of the exam, quiz and homework and store them in a separate collection.

## Total and Average of Exam 
```python
db = client.test
exam1=db.exam
exam1.count_documents({})
```
Output:
```
2
```
```python
exam1.drop()

x= db.exam_collection.aggregate([{"$match": {"scores.type":"exam"}},{ "$unwind":"$scores"},{"$match": { "scores.type":"exam" } },{"$group": {
       "_id": 'total_score_exam',
       "total_score": { "$sum": "$scores.score" } }}])
for i in x:
  i=exam1.insert_many([i])
  print(i)

x=db.exam_collection.aggregate([{'$group' : {'_id' : "avg_score_exam", "avg_score" : {'$avg' : "$scores.score"}}}])
for i in x:
  i=exam1.insert_many([i])
  print(i)
  
exam1.count_documents({})
```
Output:
```
2
```
## Total and Average of Quiz
```pythoon
db = client.test
quiz1=db.quiz
quiz1.count_documents({})
```
Output:
```
2
```
```python
quiz1.drop()

x= db.quiz_collection.aggregate([{"$match": {"scores.type":"quiz"}},{ "$unwind":"$scores"},{"$match": { "scores.type":"quiz" } },{"$group": {
       "_id": 'total_score_quiz',
       "total_score": { "$sum": "$scores.score" } }}])
for i in x:
  i=quiz1.insert_many([i])
  print(i)
  
x=db.quiz_collection.aggregate([{'$group' : {'_id' : "avg_score_quiz", "avg_score" : {'$avg' : "$scores.score"}}}])
for i in x:
  i=quiz1.insert_many([i])
  print(i)

quiz1.count_documents({})
```
Output:
```
2
```
## Total and Average for Homework
```python
db = client.test
homework1=db.homework
homework1.count_documents({})
```
Output:
```
2
```
```python
homework1.drop()

x= db.homework_collection.aggregate([{"$match": {"scores.type":"homework"}},{ "$unwind":"$scores"},{"$match": { "scores.type":"homework" } },{"$group": {
       "_id": 'total_score_homework',
       "total_score": { "$sum": "$scores.score" } }}])
for i in x:
  i=homework1.insert_many([i])
  print(i)

x=db.homework_collection.aggregate([{'$group' : {'_id' : "avg_score_homework", "avg_score" : {'$avg' : "$scores.score"}}}])
for i in x:
  i=homework1.insert_many([i])
  print(i)
  
homework1.count_documents({})
```
Output:
```
2
```
Here,
Now we can find using this code to show related seperate collection.

db.exam....this collection shows the total and average of the exam
db.quiz....this collection shows the total and average of the quiz 
db.homework....this collection shows the total and average of the homeework


# 5) Create a new collection which consists of students who scored below average and above 40% in all the categories.
## New Collection for EXAM
```python
db = client.test
gtltexam=db.gt40_ltavg_exam
gtltexam.count_documents({})
```
Output:
```
23
```
```python
gtltexam.drop()
x=db.exam_collection.find({'scores.score':{'$gte':40,'$lt':48.67367075950175}})
for i in x:
  i=gtltexam.insert_many([i])
  
gtltexam.count_documents({})
```
Output:
```
23
```
## New Collection for Quiz
```python
db = client.test
gtltquiz=db.gt40_ltavg_quiz
gtltquiz.count_documents({})
```
Output:
```
19
```
```python
gtltquiz.drop()

x=db.quiz_collection.find({'scores.score':{'$gte':40,'$lt':48.67367075950175}})
for i in x:
  i=gtltquiz.insert_many([i])
  
gtltquiz.count_documents({})
```
Output:
```
19
```
## New Collection for Homework
```python
db = client.test
gtlthomework=db.gt40_ltavg_homework
gtlthomework.count_documents({})
```
Output:
```
14
```
```python
gtlthomework.drop()

x=db.homework_collection.find({'scores.score':{'$gte':40,'$lt':48.67367075950175}})
for i in x:
  i=gtlthomework.insert_many([i])
  
gtlthomework.count_documents({})
```
Output:
```
14
```
Here,
this are the collections that created

db.gt40_ltavg_exam....this shows the collection which consists of students who scored below average and above 40% in exam.
db.gt40_ltavg_quiz....this shows the collection which consists of students who scored below average and above 40% in quiz.
db.gt40_ltavg_homework....this shows the collection which consists of students who scored below average and above 40% in homework.

# 6) Create a new collection which consists of students who scored below the fail mark in all the categories.
## New collection for Exam
```python
db = client.test
ltfailexam=db.lt_fail_exam
ltfailexam.count_documents({})
```
Output:
```
3
```
```python
ltfailexam.drop()

x=db.exam_collection.find({'scores.score':{'$lt':1}})
for i in x:
  i=ltfailexam.insert_many([i])
  
ltfailexam.count_documents({})
```
Output:
```
3
```
## New collection for Quiz
```python
db = client.test
ltfailquiz=db.lt_fail_quiz
ltfailquiz.count_documents({})
```
Output:
```
0
```
```python
ltfailquiz.drop()

x=db.quiz_collection.find({'scores.score':{'$lt':1}})
for i in x:
  i=ltfailquiz.insert_many([i])
  
ltfailquiz.count_documents({})
```
Output:
```
5
```
## New collection for Homework
```python
db = client.test
ltfailhomework=db.lt_fail_homework
ltfailhomework.count_documents({})
```
Output:
```
0
```
```python
ltfailhomework.drop()

x=db.homework_collection.find({'scores.score':{'$lt':1}})
for i in x:
  i=ltfailhomework.insert_many([i])

ltfailhomework.count_documents({})
```
Output:
```
0
```
Here,

db.lt_fail_exam...this new collection which consists of students who scored below the fail mark in exam
db.lt_fail_quiz...this new collection which consists of students who scored below the fail mark in quiz
db.lt_fail_homework...this new collection which consists of students who scored below the fail mark in homework

# 7) Create a new collection which consists of students who scored above pass mark in all the categories.
## New collection for Exam
```python
db = client.test
gtpassexam=db.gt_pass_exam
gtpassexam.count_documents({})
```
Output:
```
119
```
```python
gtpassexam.drop()

x=db.exam_collection.find({'scores.score':{'$gte':40}})
for i in x:
  i=gtpassexam.insert_many([i])
  
gtpassexam.count_documents({})
```
Output:
```
119
```
## New collection for QUIZ
```python
db = client.test
gtpassquiz=db.gt_pass_quiz
gtpassquiz.count_documents({})
```
Output:
```
114
```
```python
gtpassquiz.drop()
x=db.quiz_collection.find({'scores.score':{'$gte':40}})
for i in x:
  i=gtpassquiz.insert_many([i])
  
gtpassquiz.count_documents({})
```
Output:
```
114
```
## new collection for Homework:
```python
db = client.test
gtpasshomework=db.gt_pass_homework
gtpasshomework.count_documents({})
```
Output:
```
171
```
```
gtpasshomework.drop()
x=db.homework_collection.find({'scores.score':{'$gte':40}})
for i in x:
  i=gtpasshomework.insert_many([i])
  
gtpasshomework.count_documents({})
````
Output:
```
171
```
Here, this are the collections that are created

db.gt_pass_exam.......this new collection which consists of students who scored above pass mark in exam
db.gt_pass_quiz.......this new collection which consists of students who scored above pass mark in quiz
db.gt_pass_homework...this new collection which consists of students who scored above pass mark in homework
















The Wasmtime CLI can be installed on Linux and macOS with a small install
script:

```sh
curl https://wasmtime.dev/install.sh -sSf | bash
```

Windows or otherwise interested users can download installers and
binaries directly from the [GitHub
Releases](https://github.com/bytecodealliance/wasmtime/releases) page.

## Example

If you've got the [Rust compiler
installed](https://www.rust-lang.org/tools/install) then you can take some Rust
source code:

```rust
fn main() {
    println!("Hello, world!");
}
```

and compile/run it with:

```sh
$ rustup target add wasm32-wasi
$ rustc hello.rs --target wasm32-wasi
$ wasmtime hello.wasm
Hello, world!
```

## Features

* **Fast**. Wasmtime is built on the optimizing [Cranelift] code generator to
  quickly generate high-quality machine code either at runtime or
  ahead-of-time. Wasmtime is optimized for efficient instantiation, low-overhead
  calls between the embedder and wasm, and scalability of concurrent instances.

* **[Secure]**. Wasmtime's development is strongly focused on correctness and
  security. Building on top of Rust's runtime safety guarantees, each Wasmtime
  feature goes through careful review and consideration via an [RFC
  process]. Once features are designed and implemented, they undergo 24/7
  fuzzing donated by [Google's OSS Fuzz]. As features stabilize they become part
  of a [release][release policy], and when things go wrong we have a
  well-defined [security policy] in place to quickly mitigate and patch any
  issues. We follow best practices for defense-in-depth and integrate
  protections and mitigations for issues like Spectre. Finally, we're working to
  push the state-of-the-art by collaborating with academic researchers to
  formally verify critical parts of Wasmtime and Cranelift.

* **[Configurable]**. Wasmtime uses sensible defaults, but can also be
  configured to provide more fine-grained control over things like CPU and
  memory consumption. Whether you want to run Wasmtime in a tiny environment or
  on massive servers with many concurrent instances, we've got you covered.

* **[WASI]**. Wasmtime supports a rich set of APIs for interacting with the host
  environment through the [WASI standard](https://wasi.dev).

* **[Standards Compliant]**. Wasmtime passes the [official WebAssembly test
  suite](https://github.com/WebAssembly/testsuite), implements the [official C
  API of wasm](https://github.com/WebAssembly/wasm-c-api), and implements
  [future proposals to WebAssembly](https://github.com/WebAssembly/proposals) as
  well. Wasmtime developers are intimately engaged with the WebAssembly
  standards process all along the way too.

[Wasmtime]: https://github.com/bytecodealliance/wasmtime
[Cranelift]: https://github.com/bytecodealliance/wasmtime/blob/main/cranelift/README.md
[Google's OSS Fuzz]: https://google.github.io/oss-fuzz/
[security policy]: https://bytecodealliance.org/security
[RFC process]: https://github.com/bytecodealliance/rfcs
[release policy]: https://docs.wasmtime.dev/stability-release.html
[Secure]: https://docs.wasmtime.dev/security.html
[Configurable]: https://docs.rs/wasmtime/latest/wasmtime/struct.Config.html
[WASI]: https://docs.rs/wasmtime-wasi/latest/wasmtime_wasi/
[Standards Compliant]: https://docs.wasmtime.dev/stability-wasm-proposals-support.html

## Language Support

You can use Wasmtime from a variety of different languages through embeddings of
the implementation:

* **[Rust]** - the [`wasmtime` crate]
* **[C]** - the [`wasm.h`, `wasi.h`, and `wasmtime.h` headers][c-headers], [CMake](crates/c-api/CMakeLists.txt) or [`wasmtime` Conan package]
* **C++** - the [`wasmtime-cpp` repository][wasmtime-cpp] or use [`wasmtime-cpp` Conan package]
* **[Python]** - the [`wasmtime` PyPI package]
* **[.NET]** - the [`Wasmtime` NuGet package]
* **[Go]** - the [`wasmtime-go` repository]

[Rust]: https://bytecodealliance.github.io/wasmtime/lang-rust.html
[C]: https://bytecodealliance.github.io/wasmtime/examples-c-embed.html
[`wasmtime` crate]: https://crates.io/crates/wasmtime
[c-headers]: https://bytecodealliance.github.io/wasmtime/c-api/
[Python]: https://bytecodealliance.github.io/wasmtime/lang-python.html
[`wasmtime` PyPI package]: https://pypi.org/project/wasmtime/
[.NET]: https://bytecodealliance.github.io/wasmtime/lang-dotnet.html
[`Wasmtime` NuGet package]: https://www.nuget.org/packages/Wasmtime
[Go]: https://bytecodealliance.github.io/wasmtime/lang-go.html
[`wasmtime-go` repository]: https://pkg.go.dev/github.com/bytecodealliance/wasmtime-go
[wasmtime-cpp]: https://github.com/bytecodealliance/wasmtime-cpp
[`wasmtime` Conan package]: https://conan.io/center/wasmtime
[`wasmtime-cpp` Conan package]: https://conan.io/center/wasmtime-cpp

## Documentation

[📚 Read the Wasmtime guide here! 📚][guide]

The [wasmtime guide][guide] is the best starting point to learn about what
Wasmtime can do for you or help answer your questions about Wasmtime. If you're
curious in contributing to Wasmtime, [it can also help you do
that][contributing]!

[contributing]: https://bytecodealliance.github.io/wasmtime/contributing.html
[guide]: https://bytecodealliance.github.io/wasmtime

---

It's Wasmtime.
