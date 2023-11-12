# Aidana Kalakova
### Student in RS-school (Front-end)

---

### Contact information:

**Phone:** +7 700 282 22 77<br>
**E-mail:** aidana.amnbk@gmail.com<br>
**Telegram:** @danon_bk<br>
[LinkedIn](https://www.linkedin.com/in/aidana-kalakova/)<br>

---

### Briefly About Myself:

I've graduated from Nazarbayev University (Astana, Kazakhstan) as Electrical and Electronic Engineer for my bachalor degree and Electrical and Computer Engineer for my masters. <br>
At the beginning of my career I was working as a Research Assistant in the King Abdullah University of Science and Technology (Thuwal, Saudi Arabia), where I was working in the Clean Labs working eith microelectronics. During my working experience in the science sphere I've made 7 scientific publications in IEEE Transactions. One of the publications were certified with "Best Paper Award". <br>
After returning back to the Kazkhstan I've started my scientific career as teacher in Astana IT University for courses "Embedder systems", "Robotics" and "Scientific Writing". Working in the IT university made my come closere to the IT schere, where I become interested in the coding processes. As my transcript allowed me to teach IT courses I've become an instructor for the "Algorithms and Data Structure" course on golang programming language. <br>
After a while I've understood that coding brings me joy. And finally I've decided to quit my scientific path and start my industrial journey. I hope that study in the RS-school will give me good start as Front-End Developer.

---

### Skills and Proficiency:

- Golang, Java basics, C++ basics
- Git, GitHub
- VS Code
- SQLite basic
- Docker
- Algorithms and Data Structures

---

### Code example:

**Solving N-queen problem from LeetCode:**
*The n-queens puzzle is the problem of placing n queens on an n x n chessboard such that no two queens attack each other. Given an integer n, it is required to return all distinct solutions to the n-queens puzzle. <br>
Each solution contains a distinct board configuration of the n-queens' placement, where 'Q' and '.' both indicate a queen and an empty space, respectively.*

```golang
func solveNQueens(n int) [][]string {
    matrix:=make([][]int, n)
    for i:=0; i<n; i++{
        matrix[i] = make([]int, n)
    }
    return nQueens(matrix, 0, [][]string{})
}
func nQueens(matrix [][]int, i int, res [][]string) [][]string{
    if i == len(matrix){
        res1:=make([]string, len(matrix))
        for i:=0; i<len(matrix); i++{
            line:=""
            for j:=0; j<len(matrix[i]); j++{
                if matrix[i][j]==1{
                    line+="Q"
                } else{
                    line+="."
                }
            }
            res1[i] = line
        }        
        res = append(res, res1)
        return res
    }
    for j:=0; j<len(matrix); j++{
        if safeSpot(matrix, i, j){
            matrix[i][j] = 1
            res = nQueens(matrix, i+1, res)
            matrix[i][j] = 0
        }
    }
    return res
}
func safeSpot(matrix [][]int, r, c int) bool{
    for i:=0; i<len(matrix); i++{
        if matrix[i][c] == 1 {
            return false
        }
    }
    for j:=0; j<len(matrix); j++{
        if matrix[r][j] == 1 {
            return false
        }
    }
    for i:=0; i< len(matrix); i++{
        for j:=0; j<len(matrix); j++{
            if matrix[i][j] == 1{
                if (i-r) == (j-c) || (i - r) == -(j - c) {
                    return false
                }
            }
        }
    }
    return true
}
```
---

### Courses and Certifications:

- RS Schools Course «JavaScript/Front-end. Stage 1» (in progress)<br>
- Huawei Certification for completion "Datacom" ![Huawei Datacom](/certificats/Certificate1.png)<br>
- Huawei Certification "Huawei Certified Academy Instructor"![Huawei Instructor](/certificats/Certificate2.png)<br>

---

### Languages:

- English \- Upper-Intermediate (IELTS score 7.5)
- Kazakh \- Native
- Russian \-Fluent