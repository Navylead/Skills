# Skills
### About Me
I'm a QA tester trying to do my best in learning new skills in manual, load and automation testing)
### Skills
* **Testing theory**
* **Manual testing**
* **SQL(MySQL/Postgres):**
    * DML: select, where, order by, having, group by, join, except, insert into, update
    * DDL: create, alter, foreign key, primary key
* **JS basics**(functions, if, while, for)
* **GitHub**(repositories, branches)
* **Postman**(JS, auto tests API, collections, environments)
* **DevTools**(network, elements, console, sources, throttling, user agent)
* **Charles**(breakpoints, rewrites)
* **Android Studio**
* **JMETER(api, sql, web)**
* **JIRA**
* **JEST(Supertest)**
### Code Examples
#### SQL:
```
select project, commits, contributors, regexp_replace(address,'[0-9]','!','g') address from repositories;
```
```
select case
when sum(number1)%2=0 then (select max(number1) from numbers)
else (select min(number1) from numbers)
end number1, case 
when sum(number2)%2=0 then (select max(number2) from numbers)
else (select min(number2) from numbers)
end number2 from numbers
```
```
select monthly_salary, role_name, employee_name from employee_salary es 
join salary s on s.id = es.salary_id 
join roles_employee re on re.employee_id = es.employee_id 
join roles r on r.id = re.role_id
join employees e on e.id = es.employee_id
where role_name like '%Junior%' and role_name like '%Python%';
```
#### JEST(Supertest):
```
const request = require('supertest');
const expect = require('chai').expect;
const url = request('https://reqres.in/api');
const aut = {'email':'eve.holt@reqres.in', 'password':'cityslicka'}

describe('API', ()=>{
    it('test_1 Register', (done)=>{
        url
            .post('/register')
            .send({'email':'eve.holt@reqres.in', 'password':"pistol"})
            .expect(200)
            .expect('Content-Type', /json/)
            .end((err,res)=>{
                expect(res.body.id).to.be.equal(4);
                expect(res.body).to.have.property('token');
                if(err){
                    throw 'lol';
                }
                else console.log(res.body.token)
                done();
            })
    })
    it('test_2 Autorization', function(done){
        url
            .post('/login')
            .send(aut)
            .expect(200)
            .expect('Content-Type', /json/)
            .end(function(err,res){
                expect(res.body.token).to.be.equal('QpwL5tke4Pnpja7X4');
                expect(res.body).to.have.property('token');
                if(err) {
                    throw err;
                }
                done();
            })

    })
})
```
### Education
* [Vadim Ksendzov](https://ksendzov.com/) course
  * Manual testing
* A. Rusov youtube-course
  * Manual testing
* Magnitogorsk State Technical University
  * Mining engineer
### Languages
* **Russian** - native
* **English** - B1
