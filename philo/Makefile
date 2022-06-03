# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: mkoch <mkoch@student.21-school.ru>         +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/12/03 16:09:07 by mkoch             #+#    #+#              #
#    Updated: 2022/04/14 16:40:18 by mkoch            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = philo

SRCS =	input.c philosopher.c supervisor.c philo.c

HEADER = philo.h

OBJS = $(SRCS:%.c=%.o)

CFLAGS = -Wall -Werror -Wextra
RM = rm -f

all: $(NAME)

$(NAME): $(OBJS)
	 $(CC) $(CFLAGS) $(OBJS) -o $(NAME)

$(OBJS): $(HEADER) Makefile

%.o: %.c $(HEADER) Makefile
	$(CC) $(CFLAGS) -c $< -o $@
	
clean:
		$(RM) $(OBJS)

fclean:	clean
		$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re
