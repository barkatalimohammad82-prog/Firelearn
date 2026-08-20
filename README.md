# Firelearn
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>FireLearn Console</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:#030a12;
    color:#fff;
}

.app{
    min-height:100vh;
    display:flex;
}

/* SIDEBAR */

.sidebar{
    width:230px;
    background:#07111b;
    border-right:1px solid #24313d;
    padding:18px 12px;
    position:fixed;
    top:0;
    bottom:0;
    left:0;
}

.brand{
    display:flex;
    align-items:center;
    gap:10px;
    font-size:22px;
    font-weight:bold;
    color:#ff9d00;
    margin-bottom:28px;
}

.logo{
    width:38px;
    height:38px;
    border-radius:12px;
    background:linear-gradient(145deg,#ffca28,#ff4d00);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:22px;
}

.menu{
    list-style:none;
}

.menu li{
    padding:12px 14px;
    margin:4px 0;
    border-radius:8px;
    color:#b8c2ca;
    cursor:pointer;
    transition:.2s;
}

.menu li:hover,
.menu li.active{
    background:#8b4b0b;
    color:#fff;
}

.menu span{
    margin-right:10px;
}

/* MAIN */

.main{
    margin-left:230px;
    width:calc(100% - 230px);
}

.topbar{
    height:68px;
    border-bottom:1px solid #24313d;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 25px;
    background:#06101a;
}

.search{
    width:45%;
    background:#101b25;
    border:1px solid #263642;
    border-radius:9px;
    padding:11px 15px;
    color:white;
    outline:none;
}

.profile{
    width:38px;
    height:38px;
    border-radius:50%;
    background:#e84b30;
    display:flex;
    justify-content:center;
    align-items:center;
    font-weight:bold;
}

/* CONTENT */

.content{
    padding:25px;
}

.header{
    margin-bottom:22px;
}

.header h1{
    font-size:27px;
}

.header p{
    color:#8c9aa5;
    margin-top:6px;
}

/* CARDS */

.cards{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.card{
    background:#08141f;
    border:1px solid #24313d;
    border-radius:12px;
    padding:18px;
}

.card .icon{
    font-size:25px;
}

.card h3{
    color:#aeb8c0;
    font-size:14px;
    margin-top:10px;
}

.number{
    font-size:25px;
    font-weight:bold;
    margin-top:5px;
}

.up{
    color:#4edb66;
    font-size:13px;
    margin-top:5px;
}

/* GRID */

.grid{
    display:grid;
    grid-template-columns:2fr 1fr;
    gap:16px;
    margin-top:16px;
}

.panel{
    background:#08141f;
    border:1px solid #24313d;
    border-radius:12px;
    padding:18px;
}

.panel h2{
    font-size:17px;
    margin-bottom:18px;
}

/* CHART */

.chart{
    height:220px;
    display:flex;
    align-items:flex-end;
    gap:12px;
    padding:10px;
    border-left:1px solid #30404d;
    border-bottom:1px solid #30404d;
}

.bar{
    flex:1;
    background:linear-gradient(to top,#ff5a00,#ffb300);
    border-radius:6px 6px 0 0;
    min-height:30px;
    animation:grow .8s ease;
}

@keyframes grow{
    from{height:0}
}

/* COURSES */

.course{
    display:flex;
    justify-content:space-between;
    padding:13px 0;
    border-bottom:1px solid #1d2a35;
}

.course:last-child{
    border-bottom:0;
}

.course small{
    color:#8d9ba5;
}

/* BOTTOM GRID */

.bottom{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:16px;
    margin-top:16px;
}

.student{
    display:flex;
    align-items:center;
    gap:10px;
    padding:10px 0;
    border-bottom:1px solid #1d2a35;
}

.avatar{
    width:34px;
    height:34px;
    border-radius:50%;
    background:#253b4c;
    display:flex;
    align-items:center;
    justify-content:center;
}

.student small{
    color:#84929d;
}

/* STORAGE */

.storage{
    display:flex;
    align-items:center;
    gap:25px;
}

.circle{
    width:145px;
    height:145px;
    border-radius:50%;
    background:
        conic-gradient(
            #1685ff 0 46%,
            #42c76a 46% 69%,
            #ff9700 69% 84%,
            #45515b 84% 100%
        );
    display:flex;
    justify-content:center;
    align-items:center;
}

.circle::after{
    content:"256 GB\A Used";
    white-space:pre;
    text-align:center;
    width:90px;
    height:90px;
    border-radius:50%;
    background:#08141f;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    font-weight:bold;
}

/* FIRELEARN INFO */

.hero{
    margin-top:20px;
    background:linear-gradient(120deg,#0c1b28,#241405);
    border:1px solid #ff9800;
    border-radius:14px;
    padding:22px;
}

.hero h2{
    color:#ffae19;
    margin-bottom:8px;
}

.hero p{
    color:#b8c1c8;
    line-height:1.6;
}

/* BUTTON */

button{
    border:0;
    background:#ff7a00;
    color:#fff;
    padding:10px 16px;
    border-radius:7px;
    cursor:pointer;
}

button:hover{
    background:#ff9800;
}

/* RESPONSIVE */

@media(max-width:1000px){

    .cards{
        grid-template-columns:repeat(2,1fr);
    }

    .grid,
    .bottom{
        grid-template-columns:1fr;
    }
}

@media(max-width:700px){

    .sidebar{
        width:65px;
        padding:12px 7px;
    }

    .brand strong,
    .menu li span:last-child{
        display:none;
    }

    .brand{
        justify-content:center;
    }

    .menu li{
        text-align:center;
        padding:13px 5px;
    }

    .main{
        margin-left:65px;
        width:calc(100% - 65px);
    }

    .topbar{
        padding:0 12px;
    }

    .search{
        width:65%;
    }

    .content{
        padding:15px;
    }

    .cards{
        grid-template-columns:1fr;
    }

    .storage{
        flex-direction:column;
    }
}
</style>
</head>

<body>

<div class="app">

    <!-- SIDEBAR -->

    <aside class="sidebar">

        <div class="brand">
            <div class="logo">🔥</div>
            <strong>FireLearn</strong>
        </div>

        <ul class="menu">

            <li class="active">
                <span>🏠</span>
                <span>Overview</span>
            </li>

            <li>
                <span>👥</span>
                <span>Users</span>
            </li>

            <li>
                <span>📚</span>
                <span>Courses</span>
            </li>

            <li>
                <span>📖</span>
                <span>Lessons</span>
            </li>

            <li>
                <span>🎓</span>
                <span>Enrollments</span>
            </li>

            <li>
                <span>🗂️</span>
                <span>Categories</span>
            </li>

            <li>
                <span>⭐</span>
                <span>Reviews</span>
            </li>

            <li>
                <span>🗄️</span>
                <span>Database</span>
            </li>

            <li>
                <span>☁️</span>
                <span>Storage</span>
            </li>

            <li>
                <span>📊</span>
                <span>Analytics</span>
            </li>

            <li>
                <span>🔔</span>
                <span>Notifications</span>
            </li>

            <li>
                <span>⚙️</span>
                <span>Settings</span>
            </li>

        </ul>

    </aside>


    <!-- MAIN -->

    <main class="main">

        <header class="topbar">

            <input
                class="search"
                id="search"
                type="text"
                placeholder="Search anything..."
            >

            <div class="profile">A</div>

        </header>


        <section class="content">

            <div class="header">
                <h1>FireLearn Console</h1>
                <p>Manage your learning platform</p>
            </div>


            <!-- DASHBOARD CARDS -->

            <div class="cards">

                <div class="card">
                    <div class="icon">👥</div>
                    <h3>Users</h3>
                    <div class="number">12,560</div>
                    <div class="up">+12.5%</div>
                </div>

                <div class="card">
                    <div class="icon">📚</div>
                    <h3>Courses</h3>
                    <div class="number">320</div>
                    <div class="up">+8.2%</div>
                </div>

                <div class="card">
                    <div class="icon">🎓</div>
                    <h3>Enrollments</h3>
                    <div class="number">8,450</div>
                    <div class="up">+15.3%</div>
                </div>

                <div class="card">
                    <div class="icon">💰</div>
                    <h3>Revenue</h3>
                    <div class="number">$24,850</div>
                    <div class="up">+10.1%</div>
                </div>

            </div>


            <!-- CHART + COURSES -->

            <div class="grid">

                <div class="panel">

                    <h2>Learning Activity — 7 Days</h2>

                    <div class="chart">

                        <div class="bar" style="height:35%"></div>
                        <div class="bar" style="height:55%"></div>
                        <div class="bar" style="height:48%"></div>
                        <div class="bar" style="height:72%"></div>
                        <div class="bar" style="height:57%"></div>
                        <div class="bar" style="height:82%"></div>
                        <div class="bar" style="height:96%"></div>

                    </div>

                </div>


                <div class="panel">

                    <h2>Top Courses</h2>

                    <div class="course">
                        <div>
                            <b>Flutter for Beginners</b><br>
                            <small>4,850 Enrollments</small>
                        </div>
                        ⭐
                    </div>

                    <div class="course">
                        <div>
                            <b>Python Basics</b><br>
                            <small>3,420 Enrollments</small>
                        </div>
                        ⭐
                    </div>

                    <div class="course">
                        <div>
                            <b>Web Development</b><br>
                            <small>2,650 Enrollments</small>
                        </div>
                        ⭐
                    </div>

                    <div class="course">
                        <div>
                            <b>UI/UX Design</b><br>
                            <small>1,980 Enrollments</small>
                        </div>
                        ⭐
                    </div>

                    <div class="course">
                        <div>
                            <b>Digital Marketing</b><br>
                            <small>1,450 Enrollments</small>
                        </div>
                        ⭐
                    </div>

                </div>

            </div>


            <!-- BOTTOM -->

            <div class="bottom">

                <div class="panel">

                    <h2>Recent Enrollments</h2>

                    <div class="student">
                        <div class="avatar">R</div>
                        <div>
                            <b>Rohit Sharma</b><br>
                            <small>Flutter for Beginners</small>
                        </div>
                    </div>

                    <div class="student">
                        <div class="avatar">A</div>
                        <div>
                            <b>Anjali Verma</b><br>
                            <small>Python Basics</small>
                        </div>
                    </div>

                    <div class="student">
                        <div class="avatar">A</div>
                        <div>
                            <b>Aman Singh</b><br>
                            <small>Web Development</small>
                        </div>
                    </div>

                    <div class="student">
                        <div class="avatar">N</div>
                        <div>
                            <b>Neha Patel</b><br>
                            <small>UI/UX Design</small>
                        </div>
                    </div>

                </div>


                <div class="panel">

                    <h2>Storage Usage</h2>

                    <div class="storage">

                        <div class="circle"></div>

                        <div>
                            <p>🔵 Videos — 120 GB</p>
                            <br>
                            <p>🟢 Documents — 60 GB</p>
                            <br>
                            <p>🟠 Images — 40 GB</p>
                            <br>
                            <p>⚪ Others — 36 GB</p>
                        </div>

                    </div>

                </div>

            </div>


            <!-- FIRELEARN INFO -->

            <div class="hero">

                <h2>🔥 FireLearn — A Smarter Way to Build Learning Apps!</h2>

                <p>
                    Firebase जैसा, पर Learning के लिए.
                    Authentication, Database, Storage, Hosting,
                    Analytics, Notifications और AI Tutor को एक
                    learning-focused platform में manage करें.
                </p>

                <br>

                <button onclick="showMessage()">
                    Explore FireLearn
                </button>

            </div>

        </section>

    </main>

</div>


<script>

function showMessage(){

    alert(
        "🔥 Welcome to FireLearn!\n\n" +
        "Learn • Build • Grow"
    );

}


/* SEARCH */

const search = document.getElementById("search");

search.addEventListener("input", function(){

    const value = this.value.toLowerCase();

    const courses = document.querySelectorAll(".course");

    courses.forEach(course => {

        if(course.innerText.toLowerCase().includes(value)){
            course.style.display = "flex";
        }
        else{
            course.style.display = "none";
        }

    });

});


/* SIDEBAR */

document.querySelectorAll(".menu li").forEach(item => {

    item.addEventListener("click", function(){

        document
        .querySelectorAll(".menu li")
        .forEach(x => x.classList.remove("active"));

        this.classList.add("active");

    });

});

</script>

</body>
</html>
____________main.dark______________
import 'package:flutter/material.dart';

void main() {
  runApp(const FireLearnApp());
}

class FireLearnApp extends StatelessWidget {
  const FireLearnApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'FireLearn',
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: const Color(0xFF030A12),
        colorScheme: ColorScheme.fromSeed(
          seedColor: Colors.orange,
          brightness: Brightness.dark,
        ),
      ),
      home: const FireLearnDashboard(),
    );
  }
}

class FireLearnDashboard extends StatelessWidget {
  const FireLearnDashboard({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: const Color(0xFF06101A),
        title: const Row(
          children: [
            Text("🔥"),
            SizedBox(width: 8),
            Text(
              "FireLearn",
              style: TextStyle(
                color: Colors.orange,
                fontWeight: FontWeight.bold,
              ),
            ),
            Text(" Console"),
          ],
        ),
        actions: [
          IconButton(
            onPressed: () {},
            icon: const Icon(Icons.notifications_outlined),
          ),
          const Padding(
            padding: EdgeInsets.only(right: 15),
            child: CircleAvatar(
              backgroundColor: Colors.deepOrange,
              child: Text("A"),
            ),
          ),
        ],
      ),

      drawer: const FireLearnDrawer(),

      body: SingleChildScrollView(
        padding: const EdgeInsets.all(16),
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [

            const Text(
              "Overview",
              style: TextStyle(
                fontSize: 28,
                fontWeight: FontWeight.bold,
              ),
            ),

            const SizedBox(height: 5),

            const Text(
              "Manage your learning platform",
              style: TextStyle(color: Colors.grey),
            ),

            const SizedBox(height: 20),

            GridView.count(
              crossAxisCount: 2,
              shrinkWrap: true,
              physics: const NeverScrollableScrollPhysics(),
              crossAxisSpacing: 12,
              mainAxisSpacing: 12,
              childAspectRatio: 1.5,
              children: const [
                StatCard(
                  icon: Icons.people,
                  title: "Users",
                  value: "12,560",
                  growth: "+12.5%",
                ),
                StatCard(
                  icon: Icons.menu_book,
                  title: "Courses",
                  value: "320",
                  growth: "+8.2%",
                ),
                StatCard(
                  icon: Icons.school,
                  title: "Enrollments",
                  value: "8,450",
                  growth: "+15.3%",
                ),
                StatCard(
                  icon: Icons.attach_money,
                  title: "Revenue",
                  value: "\$24,850",
                  growth: "+10.1%",
                ),
              ],
            ),

            const SizedBox(height: 20),

            const DashboardPanel(
              title: "📈 Learning Activity — 7 Days",
              child: ActivityChart(),
            ),

            const SizedBox(height: 16),

            const DashboardPanel(
              title: "📚 Top Courses",
              child: Column(
                children: [
                  CourseItem(
                    title: "Flutter for Beginners",
                    students: "4,850 Enrollments",
                  ),
                  CourseItem(
                    title: "Python Basics",
                    students: "3,420 Enrollments",
                  ),
                  CourseItem(
                    title: "Web Development",
                    students: "2,650 Enrollments",
                  ),
                  CourseItem(
                    title: "UI/UX Design",
                    students: "1,980 Enrollments",
                  ),
                  CourseItem(
                    title: "Digital Marketing",
                    students: "1,450 Enrollments",
                  ),
                ],
              ),
            ),

            const SizedBox(height: 16),

            const DashboardPanel(
              title: "👨‍🎓 Recent Enrollments",
              child: Column(
                children: [
                  StudentItem(
                    name: "Rohit Sharma",
                    course: "Flutter for Beginners",
                  ),
                  StudentItem(
                    name: "Anjali Verma",
                    course: "Python Basics",
                  ),
                  StudentItem(
                    name: "Aman Singh",
                    course: "Web Development",
                  ),
                  StudentItem(
                    name: "Neha Patel",
                    course: "UI/UX Design",
                  ),
                ],
              ),
            ),

            const SizedBox(height: 16),

            const DashboardPanel(
              title: "💾 Storage Usage",
              child: StorageWidget(),
            ),

            const SizedBox(height: 16),

            Container(
              width: double.infinity,
              padding: const EdgeInsets.all(20),
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(16),
                border: Border.all(color: Colors.orange),
                gradient: const LinearGradient(
                  colors: [
                    Color(0xFF0C1B28),
                    Color(0xFF241405),
                  ],
                ),
              ),
              child: const Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Text(
                    "🔥 FireLearn",
                    style: TextStyle(
                      fontSize: 23,
                      color: Colors.orange,
                      fontWeight: FontWeight.bold,
                    ),
                  ),
                  SizedBox(height: 8),
                  Text(
                    "Firebase जैसा, पर Learning के लिए.",
                    style: TextStyle(fontSize: 17),
                  ),
                  SizedBox(height: 8),
                  Text(
                    "Authentication • Database • Storage • Hosting • "
                    "Analytics • Notifications • AI Tutor",
                    style: TextStyle(color: Colors.grey),
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}


/* DRAWER */

class FireLearnDrawer extends StatelessWidget {
  const FireLearnDrawer({super.key});

  @override
  Widget build(BuildContext context) {
    return Drawer(
      backgroundColor: const Color(0xFF07111B),
      child: ListView(
        children: [

          const DrawerHeader(
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                Text(
                  "🔥",
                  style: TextStyle(fontSize: 45),
                ),
                Text(
                  "FireLearn",
                  style: TextStyle(
                    color: Colors.orange,
                    fontSize: 25,
                    fontWeight: FontWeight.bold,
                  ),
                ),
                Text("Learn • Build • Grow"),
              ],
            ),
          ),

          menu(Icons.dashboard, "Overview"),
          menu(Icons.people, "Users"),
          menu(Icons.menu_book, "Courses"),
          menu(Icons.book, "Lessons"),
          menu(Icons.school, "Enrollments"),
          menu(Icons.category, "Categories"),
          menu(Icons.star, "Reviews"),
          menu(Icons.storage, "Database"),
          menu(Icons.cloud, "Storage"),
          menu(Icons.analytics, "Analytics"),
          menu(Icons.notifications, "Notifications"),
          menu(Icons.settings, "Settings"),
        ],
      ),
    );
  }

  Widget menu(IconData icon, String title) {
    return ListTile(
      leading: Icon(icon),
      title: Text(title),
      onTap: () {},
    );
  }
}


/* STAT CARD */

class StatCard extends StatelessWidget {
  final IconData icon;
  final String title;
  final String value;
  final String growth;

  const StatCard({
    super.key,
    required this.icon,
    required this.title,
    required this.value,
    required this.growth,
  });

  @override
  Widget build(BuildContext context) {
    return Container(
      padding: const EdgeInsets.all(15),
      decoration: BoxDecoration(
        color: const Color(0xFF08141F),
        borderRadius: BorderRadius.circular(14),
        border: Border.all(color: const Color(0xFF24313D)),
      ),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Icon(
            icon,
            color: Colors.orange,
            size: 28,
          ),
          const SizedBox(height: 8),
          Text(
            title,
            style: const TextStyle(color: Colors.grey),
          ),
          Text(
            value,
            style: const TextStyle(
              fontSize: 21,
              fontWeight: FontWeight.bold,
            ),
          ),
          Text(
            growth,
            style: const TextStyle(
              color: Colors.greenAccent,
            ),
          ),
        ],
      ),
    );
  }
}


/* PANEL */

class DashboardPanel extends StatelessWidget {
  final String title;
  final Widget child;

  const DashboardPanel({
    super.key,
    required this.title,
    required this.child,
  });

  @override
  Widget build(BuildContext context) {
    return Container(
      width: double.infinity,
      padding: const EdgeInsets.all(18),
      decoration: BoxDecoration(
        color: const Color(0xFF08141F),
        borderRadius: BorderRadius.circular(14),
        border: Border.all(color: const Color(0xFF24313D)),
      ),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Text(
            title,
            style: const TextStyle(
              fontSize: 18,
              fontWeight: FontWeight.bold,
            ),
          ),
          const SizedBox(height: 16),
          child,
        ],
      ),
    );
  }
}


/* ACTIVITY CHART */

class ActivityChart extends StatelessWidget {
  const ActivityChart({super.key});

  @override
  Widget build(BuildContext context) {
    final values = [0.35, 0.55, 0.48, 0.72, 0.57, 0.82, 0.96];

    return SizedBox(
      height: 190,
      child: Row(
        crossAxisAlignment: CrossAxisAlignment.end,
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: values.map((value) {
          return Container(
            width: 25,
            height: 160 * value,
            decoration: BoxDecoration(
              borderRadius: BorderRadius.circular(6),
              gradient: const LinearGradient(
                begin: Alignment.bottomCenter,
                end: Alignment.topCenter,
                colors: [
                  Colors.deepOrange,
                  Colors.orange,
                ],
              ),
            ),
          );
        }).toList(),
      ),
    );
  }
}


/* COURSE */

class CourseItem extends StatelessWidget {
  final String title;
  final String students;

  const CourseItem({
    super.key,
    required this.title,
    required this.students,
  });

  @override
  Widget build(BuildContext context) {
    return ListTile(
      contentPadding: EdgeInsets.zero,
      leading: const CircleAvatar(
        backgroundColor: Colors.orange,
        child: Icon(
          Icons.play_arrow,
          color: Colors.white,
        ),
      ),
      title: Text(title),
      subtitle: Text(students),
      trailing: const Icon(
        Icons.star,
        color: Colors.orange,
      ),
    );
  }
}


/* STUDENT */

class StudentItem extends StatelessWidget {
  final String name;
  final String course;

  const StudentItem({
    super.key,
    required this.name,
    required this.course,
  });

  @override
  Widget build(BuildContext context) {
    return ListTile(
      contentPadding: EdgeInsets.zero,
      leading: CircleAvatar(
        backgroundColor: Colors.blueGrey.shade700,
        child: Text(name[0]),
      ),
      title: Text(name),
      subtitle: Text(course),
    );
  }
}


/* STORAGE */

class StorageWidget extends StatelessWidget {
  const StorageWidget({super.key});

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [

        const SizedBox(
          height: 150,
          width: 150,
          child: CircularProgressIndicator(
            value: .72,
            strokeWidth: 18,
            color: Colors.orange,
            backgroundColor: Colors.blueGrey,
          ),
        ),

        const SizedBox(height: 15),

        const Text(
          "256 GB Used",
          style: TextStyle(
            fontSize: 20,
            fontWeight: FontWeight.bold,
          ),
        ),

        const SizedBox(height: 15),

        const Text("🔵 Videos — 120 GB"),
        const Text("🟢 Documents — 60 GB"),
        const Text("🟠 Images — 40 GB"),
        const Text("⚪ Others — 36 GB"),
      ],
    );
  }
}
