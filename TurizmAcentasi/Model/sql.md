otel sorgu :
CREATE TABLE `otel` (
`id` int NOT NULL AUTO_INCREMENT,
`name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`star` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`property` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`address` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`phone` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`mail` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=41 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

reservation_info sorgu :
CREATE TABLE `reservation_info` (
`id` int NOT NULL AUTO_INCREMENT,
`client_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`client_phone` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`client_mail` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`client_note` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`room_id` int NOT NULL,
`check_in` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`check_out` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`adult_num` int NOT NULL,
`child_num` int NOT NULL,
`total_price` int NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

room sorgu :

CREATE TABLE `room` (
`id` int NOT NULL AUTO_INCREMENT,
`room_type` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`stock` int NOT NULL,
`season_id` int NOT NULL,
`adult_price` int NOT NULL,
`child_price` int NOT NULL,
`otel_type_id` int NOT NULL,
`otel_id` int NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=20 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

room_property sorgu:

CREATE TABLE `room_property` (
`id` int NOT NULL AUTO_INCREMENT,
`property` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`room_id` int NOT NULL,
`bed` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`area` int NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

season sorgu :

CREATE TABLE `season` (
`id` int NOT NULL AUTO_INCREMENT,
`season_start` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`season_end` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`otel_id` int NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=19 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

type_otel sorgu :
CREATE TABLE `type_otel` (
`id` int NOT NULL AUTO_INCREMENT,
`type` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`otel_id` int NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=43 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

user sorgu :

CREATE TABLE `user` (
`id` int NOT NULL AUTO_INCREMENT,
`name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`username` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`password` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`type` enum('Admin','Employee') CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=17 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci
