import { Component, OnInit } from '@angular/core';
import { TodoListItem } from './models';
import { ListDataService } from './services/list-data.service';
import { Observable } from 'rxjs';

@Component({
  selector: 'app-todo',
  templateUrl: './todo.component.html',
  styleUrls: ['./todo.component.css']
})
export class TodoComponent implements OnInit {

  toDoList$: Observable<TodoListItem[]>;

  constructor(private service: ListDataService) { }

  ngOnInit() {
    this.toDoList$ = this.service.getData();
    // this.service.getData().subscribe(stuff => {
    // console.log('from service', stuff);
    // this.toDoList = stuff;
    // });
  }

  addTodoItem(what: string) {
    this.service.add(what);
  }

}
