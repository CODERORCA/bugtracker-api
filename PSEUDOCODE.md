## Pseudocodes
### Repository Layer
class userRepo
	// find user
	function findUserId(userId)"
		return.db.select("users", where id = userId)
	
	// find user by email
	function findEmail(email):
		return.db.select("users", where id = email)

class projectRepo
	//find project
	function findProjectId(projectId)
		return.db.select("project", where id = projectId)
	
	// check if user is assigned
	function userAssigned(projectId, userId):
		return.db.exists("project_users", where project_id = projectID AND user_id = userId)

class ticketRepo:
	// save tickets
	function save(ticket):
		db.insert("tickets", ticket)
		return ticket.id
	
	// find tickets
	function findTicketId(ticketId):
		return db.select("tickets", where id = ticketId)
	
	// update tickets
	function updateTicket(ticketId, status):
		db.update("tickets", id = ticketId, set status = status)
		return db.select("tickets", where id = ticketId)

### Service Layer
class ticketService:
	// construct Ticket repo
	constructor(repository: ticketRepository)
		this.repository = repository
	
	// create new ticket
	function createTicket(user, project, title, description):
		if title is empty or description is empty:
			raise validationError("Title or description required")
		
		// Dict of required items
		ticket = Ticket{
		title = title,
		description = description
		projectId = project.id
		userId = user.id
		status = "open"
		}
		
		// save Dict into the repo
		ticketId = this.repository.save(ticket)
		return this.respository.findTicketId(ticketId)
	
	// update status of ticket
	function changeTicket(user, ticketId, newStatus):
		ticket = this.respository.findTicketId(ticketId)
		if user.role not in ["Admin", "Assignee"]:
			raise permissionError("Unauthorized User")
		
		this.repository.updateStatus(ticketId, newStatus)
		return this.repository.findTicketId(ticketID)

### API Layer
// handler for user authentication via token
function handleCreateTicket(request):
	user = authenticate(request.token)
	ticketService = TicketService(ticketRepository())
	ticket = ticketService.createTicket(user, request.project, request.title, request.description)
	return Response(201, ticket)

// handler for ticket updates
function handleUpdateTicket(request):
	user: authenticate(request.toke)
	ticketService = TicketService(ticketRepo())
	ticket = ticketService.updateTicket(user, request.ticketId, request.newStatus)
	return Response(200, ticket)

