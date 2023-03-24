# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: jde-orma <jde-orma@42urduliz.com>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/03/17 10:51:06 by jde-orma          #+#    #+#              #
#    Updated: 2023/03/17 10:51:06 by jde-orma         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# Coder Alias

USER_NAME	=	jde-orma

# Compiler, flags and static library ceation

CC			=	gcc
CCFLAGS		=	-Wall -Wextra -Werror
AR			=	ar rc
RM			=	rm -f

# **************************************************************************** #

# Code implementation NAME

CODE		=	ft_printf

# Static library names:

NAME		=	libftprintf.a
LIBFT_FILE	=	libft.a

# File directories

INCLUDES	=	include/
LIBFT_DIR	=	libft/
SRC_DIR		=	source/

# Source Files:

SRC_FILES	=	ft_printf.c

# Source && static library files + directories

LIBFT		=	$(addprefix $(LIBFT_DIR), $(LIBFT_FILE))
SRC			=	$(addprefix $(SRC_DIR), $(SRC_FILES))

# Object files creation

OBJ			=	$(SRC:.c=.o)

#Colors:

DEF_COLOR	=	\033[0;39m
WHITE		=	\033[0;97m
BLUE		=	\033[0;94m
GREEN		=	\033[0;92m

# **************************************************************************** #

all:		$(LIBFT) $(NAME)

$(NAME):	$(OBJ)
			@cp $(LIBFT) $(NAME)
			@$(AR) $(NAME) $(OBJ)
			@echo "$(GREEN)✔ $(BLUE)$(USER_NAME)'s $(CODE) compilation$(DEF_COLOR)"


$(LIBFT):
			@make -C ./libft

.c.o:
			@$(CC) $(CCFLAGS) -I$(INCLUDES) -c $< -o $(<:.c=.o)

clean:
			@$(RM) $(OBJ)
			@echo "$(GREEN)✔ $(BLUE)$(USER_NAME)'s $(CODE) .o files removal$(WHITE)"
			@if [ "$(CLEAN_CALLED_FROM_FCLEAN)" != "1" ]; then \
				make clean -C ./libft; \
			fi

fclean:
			@$(MAKE) CLEAN_CALLED_FROM_FCLEAN=1 clean
			@make fclean -C ./libft
			@$(RM) $(NAME)
			@echo "$(GREEN)✔ $(BLUE)$(USER_NAME)'s $(NAME) removal$(DEF_COLOR)"

re:			fclean all

.PHONY:		all clean fclean re libft
