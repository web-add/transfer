if (Server_Security.login_time + 6500 < (duration_cast<milliseconds>(system_clock::now().time_since_epoch())).count()) {
				Server_Security.login_count = 0;
				Server_Security.update_item_data = 0;
				Server_Security.login_time = (duration_cast<milliseconds>(system_clock::now().time_since_epoch())).count();
}
if (Server_Security.login_count < 40 || Server_Security.update_item_data < 15) {
				for (ENetPeer* currentPeer = server->peers; currentPeer < &server->peers[server->peerCount]; ++currentPeer) {
					if (currentPeer->state != ENET_PEER_STATE_CONNECTED or currentPeer->data == NULL or clientConnection != pInfo(currentPeer)->ip) continue;
					logged++;
				}
}
if (logged >= 3 || Server_Security.login_count > 40 || Server_Security.update_item_data > 15) {
				failed_login(peer, "CT:[S]_ `4OOPS:`` Too many people logging in at once. Please press `5CANCEL`` and try again in a few seconds.");
				break;
}
