# final-project
import { useState } from "react";

function App() {
  const [page, setPage] = useState("home");
  const [count, setCount] = useState(0);

  return (
    <div className="flex flex-col items-center gap-4 p-6">
      {page === "home" && (
        <>
          <h1 className="text-2xl font-bold">Welcome</h1>
          <button onClick={() => setPage("login")} className="px-4 py-2 bg-blue-500 text-white rounded">Go to Login</button>
          <button onClick={() => setPage("game")} className="px-4 py-2 bg-green-500 text-white rounded">Go to Game</button>
        </>
      )}

      {page === "login" && (
        <>
          <h1 className="text-2xl font-bold">Login</h1>
          <input type="text" placeholder="Username" className="p-2 border rounded" />
          <input type="password" placeholder="Password" className="p-2 border rounded" />
          <button className="px-4 py-2 bg-blue-500 text-white rounded">Login</button>
          <button onClick={() => setPage("home")} className="px-4 py-2 bg-gray-500 text-white rounded">Back</button>
        </>
      )}

      {page === "game" && (
        <>
          <h1 className="text-2xl font-bold">Click Counter Game</h1>
          <p className="text-xl">Count: {count}</p>
          <button onClick={() => setCount(count + 1)} className="px-4 py-2 bg-green-500 text-white rounded">Click Me</button>
          <button onClick={() => setPage("home")} className="px-4 py-2 bg-gray-500 text-white rounded">Back</button>
        </>
      )}
    </div>
  );
}

export default App;
