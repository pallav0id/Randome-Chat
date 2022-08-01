# Randome-Chat
<!DOCTYPE html>
<html lang="fr">

<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.css" type="text/css"
		rel="stylesheet" </head>
	<link href="//maxcdn.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css" rel="stylesheet" id="bootstrap-css">
	<link rel="stylesheet" href="css/style.css" />
	<link rel="stylesheet" href="css/uikit.min.css" />
	<script src="js/uikit.min.js"></script>
	<script src="js/uikit-icons.min.js"></script>
	<script src="//maxcdn.bootstrapcdn.com/bootstrap/4.1.1/js/bootstrap.min.js"></script>
	<title>Random chat</title>
	<meta name="description" content="Random Chat: connectez-vous \
		pour discuter avec des ENSTA en toute anonymat..." />
</head>

<body>
	<!-- Welcomme page overlay -->
	<div id="welcomePage" class="overlay">
		<div id="welcomeTitleContainer">
			<div id="welcomeTitle">
				<h1>Yōkoso Connecting Chat!</h1>
			</div>
			<div id="connectButton">
				<button class="uk-button-primary uk-button-large" onclick="connect()">Connector</button>
			</div>
		</div>
	</div>
	<!-- Username form page overlay -->
	<div id="usernameFormPage" class="overlay">
		<div class="form">
			<h3 class="title">Your Name?</h3>
			<input id="usernameInputField" class="usernameInput" type="text" maxlength="14" autofocus />
		</div>
	</div>
	<!-- Spinner page overlay -->
	<div id="spinnerPage" class="overlay">
		<div class="roomWaitMessage">
			<h3 class="title">En attente de salon...</h3>
			<div id="spinner" uk-spinner="ratio: 3"></div>
		</div>
	</div>
	<!-- Chat page -->
	<div class="container">
		<h3 id="interloc" class=" text-center"></h3>
		<!-- connected people live counter -->
		<p id="peopleCounter"></p>
		<div class="messaging">
			<div class="inbox_msg">
				<div class="mesgs">
					<!-- messaging history -->
					<div class="msg_history" id="messages">
					</div>
					<!-- input form -->
					<div class="type_msg">
						<div class="input_msg_write">
							<textarea rows="1" type="text" class="write_msg" id="userMessageInputField"
								placeholder="type your message"></textarea>
						</div>
						<button class="msg_send_btn" uk-tooltip="title: Alors ? On hésite ?; delay: 5000" type="button"
							onclick="sendMessage(socket)"><i class="fa fa-paper-plane-o" aria-hidden="true"></i></button>
					</div>
				</div>
			</div>
		</div>
	</div>
	<!-- js -->
	<script src="/socket.io/socket.io.js"></script>
	<script src="js/init.js"></script>
</body>

</html>
