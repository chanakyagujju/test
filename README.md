Description :

	This test case will test throttler with burst of 100 notifications from rabbitmq with 1 almond, 1 device, device type 1.

-----------------------------------------------------------------------------------------

How to use?

	bash$: RAMMITMQ_QUEUE=throttler_test node send_notification.js
	
	above command will send 100 dummy notifications to rabbitmq, after all notifications are sent then,
	
	bash$: RABBITMQ_QUEUE=throttler_test node test_01_app.js
	
------------------------------------------------------------------------------------------

Expected output :

	Received messages :
		message : 1
		message : 2
		message : 3
		message : 4
		message : 5
		.
		.
		(delay of Token updater time)
		.
		.
		message : 98
		.
		.
		(delay of Token updater time)
		.
		.
		message : 99
		.
		.
		(delay of Token updater time)
		.
		.
		message : 100
		
test issue1		
