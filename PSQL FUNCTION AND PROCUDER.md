# TASK_1
```SQL
create or replace function Task_1(a varchar)
    returns text
    language  plpgsql
as
$$
declare
    result varchar;
 begin
    select model::json ->> a
    into result
    from aircrafts_data;
    return result;
end;
$$;

select Task_1('en');
select Task_1('ru');
```
ENGLISH
![image](https://user-images.githubusercontent.com/122611553/225217620-965dec49-c59f-472b-bbca-294ac68caadd.png)

RUSSAIN
![image](https://user-images.githubusercontent.com/122611553/225217435-236ba2a9-13b7-42fd-b1fa-784f679f3cab.png)


