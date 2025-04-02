a l t s
import { Component } from '@angular/core';
import { Router } from '@angular/router';
// import { AuthGuard} from '../auth.guard';

@Component({
  selector: 'app-admin-login',
  templateUrl: './admin-login.component.html',
  styleUrls: ['./admin-login.component.css']
})
export class AdminLoginComponent {
username ='';
password='';
//errorMessage='';

constructor(private router: Router){}
login(){
  if(this.username==='admin' && this.password==='admin123'){
    console.log("Login successful ! Redirecting...");
    this.router.navigate(['/admin']);
  }
  else{
    alert('Invalid username or password');
  }
}
}



a l hl

<div class="login-container">
    <h2>Admin Login</h2>
        <input type="text" [(ngModel)]="username" placeholder="Username"/>
        <input type="password" [(ngModel)]="password" placeholder="Password"/>
        <button (click)="login()">Login as Admin</button>
        <!-- <p *ngIf="errorMessage" style="color: red;">{{ errorMessage }}</p> -->
</div>
