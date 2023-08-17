# Load Balancer with Round Robin

This is a Load Balancer project implemented in Go that uses a round-robin algorithm to distribute incoming HTTP requests across multiple backend servers. The load balancer aims to evenly distribute the traffic to provide better performance and high availability.

## Usage

1. Clone the repository:

   ```sh
   git clone https://github.com/ritikchawla/LoadBalancer.git
   cd LoadBalancer
   ```
2.  Build and run the load balancer:
    
    
    `go run main.go` 
    
3.  Open your web browser and navigate to [http://localhost:8000](http://localhost:8000/) to access the load-balanced content.
    

## How It Works

The load balancer distributes incoming requests to a set of backend servers using a round-robin approach. Each incoming request is forwarded to the next available server in the rotation, providing an even distribution of the workload.

### Load Balancer Configuration

The configuration of backend servers is done in the `main` function of `main.go`. You can add or remove backend servers as needed:


`servers := [] Server{
    newSimpleServer("https://www.google.com"),
    newSimpleServer("https://www.duckduckgo.com"),
    newSimpleServer("https://www.bing.com"),
}` 

### Round Robin Algorithm

The round-robin algorithm is implemented in the `LoadBalancer` struct. It maintains a counter to keep track of the next server to which a request should be forwarded. Requests are distributed evenly among the available servers.

### Error Handling

The load balancer includes basic error handling to handle unavailable servers and potential errors.

## Thanks
I am passionate about exploring new technologies and creating exciting projects. If you have interesting project ideas and would like to collaborate, feel free to reach out to me via [email](mailto:chawlaritik@gmail.com).