# ts

1.
interface User {
    id: number;
    name: string;
    age: number;
    email: string;
    phones?: string[];
}

let users: User[] = [
    { id: 1, name: "John Doe", age: 25, email: "john@example.com" },
    { id: 2, name: "Alice Smith", age: 30, email: "alice@example.com" },
    { id: 3, name: "Bob Johnson", age: 28, email: "bob@example.com" }
];

2.
function filterUsersByAge(users: User[], minAge: number): User[] {
    return users.filter(user => user.age > minAge);
}

let filteredUsers = filterUsersByAge(users, 28);

console.log(filteredUsers);

3.
enum UserRole {
    Admin,
    Moderator,
    User
}

interface User {
    id: number;
    name: string;
    age: number;
    email: string;
    role: UserRole;
}

// Создание массива пользователей с использованием интерфейса User и перечисления UserRole
let users: User[] = [
    { id: 1, name: "John Doe", age: 25, email: "john@example.com", role: UserRole.User },
    { id: 2, name: "Alice Smith", age: 30, email: "alice@example.com", role: UserRole.Moderator },
    { id: 3, name: "Bob Johnson", age: 28, email: "bob@example.com", role: UserRole.Admin }
];

4.
function checkAccess(user: User, requiredRole: UserRole): boolean {
    return user.role === requiredRole;
}

let currentUser: User = users[0];
let hasAdminAccess: boolean = checkAccess(currentUser, UserRole.Admin);

