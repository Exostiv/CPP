# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: tnicoue <tnicoue@student.42.fr>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/09/27 12:16:04 by tnicoue           #+#    #+#              #
#    Updated: 2022/09/27 12:16:05 by tnicoue          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC = g++

RM = rm -f

CFLAGS = -Wall -Wextra -Werror -std=c++98 

NAME = zomb 

SRCDIR = ./srcs

SRC = $(wildcard *.cpp)

OBJ = $(SRC:.cpp=.o)

all:
	@$(MAKE) -j $(NAME)	

$(NAME): $(SRC)
	$(CC) $(CFLAGS) $(SRC) -o $(NAME)

%.o : %.cpp
	$(CC) -c $(CFLAGS) $(SRC) $< -o $@ 

clean:
	$(RM) $(OBJ)

fclean: clean
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re