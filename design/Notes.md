
# Structural

* Player
  * id
  * first_name
  * last_name
  * statistics

* Team
  * id
  * team_name
  * player_ids

* Game
  * id
  * player_or_team_ids
  * team_game
  * game_status

* Statistics
  * player_id
  * games_played
  * games_won
  * games_lost
  * win_percentage
  * loss_percentage

* Tournament
  * id
  * game_ids
  * team_ids
  * tournament_status
  * winner_id
