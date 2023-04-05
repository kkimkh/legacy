-- 계정 생성하기
create database db_codingrecipe;
create user user_codingrecipe@localhost identified by '1234';
grant all privileges on db_codingrecipe.* to user_codingrecipe@localhost;

-- 회원 테이블
drop table if exists member_table;
create table member_table(
id bigint primary key auto_increment,
memberEmail varchar(20) unique,
memberPassword varchar(20),
memberName varchar(20),
memberAge int,
memberMobile varchar(30)
); 